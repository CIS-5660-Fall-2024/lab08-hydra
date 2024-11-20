# Lab 08 - Creative Coding with Hydra
   
## Lab Puzzles:
The goal of each puzzle will be to replicate the look of each puzzle’s image by exploring the hydra api.

### 1. Puzzle 1: You're getting sleepy

![d2765d83f53a79102bbee596dc137abf](https://github.com/user-attachments/assets/a5f6f0da-5ca7-4066-9ceb-8851c2a14071)

Solution: https://hydra.ojack.xyz/?sketch_id=qg1UNGtEM410YZu1

```js
shape(99, 0.5, 0)
  .mask(osc(16,-0.1,0.5).scale(0.2).kaleid(50))
  .color(1,0,1)
  .scrollX([-0.2,0.2].smooth())
  .out(o0)

render(o0)
```

### 2. Puzzle 2: Dancing Squares
[![Image from Gyazo](https://i.gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51.gif)](https://gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51)

Solution: https://hydra.ojack.xyz/?sketch_id=8nI5CHLl837Dae1f

```js
const THREE = await import("https://unpkg.com/three@0.163.0/build/three.module.js")

scene = new THREE.Scene()
camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000)

renderer = new THREE.WebGLRenderer()
renderer.setSize(width, height)
geometry = new THREE.BoxGeometry()
material = new THREE.MeshBasicMaterial({color: 0x00ff00})
cube = new THREE.Mesh(geometry, material);
scene.add(cube)
camera.position.z = 1.5

// 'update' is a reserved function that will be run every time the main hydra rendering context is updated
update = () => {
  cube.rotation.y += 0.02;
  cube.rotation.x += 0.02;
  renderer.render( scene, camera );
}

s0.init({ src: renderer.domElement })

src(s0)
  .repeat(3, 3)
  .out()
```
     
### 3. Your own cool effect!

Solution: https://hydra.ojack.xyz/?sketch_id=9a2W0BXLWvGda9Ji

```js
shape(4,0.96)
  .repeat(12,12).invert().color(1,0,1)
  .scrollY(0,0.05)
  .modulate(osc(60, 0.05, 0).kaleid(100))
  .add(
    shape(4,0.96)
    .repeat(12,12).invert().color(0, 1, 1)
    .scrollY(0,-0.05)
    .modulate(osc(60, 0.05, 0).kaleid(100))
  	.scrollX(0.2)
  )
  .add(
    shape(4,0.96)
    .repeat(12,12).invert().color(1, 1, 0)
    .scrollY(0,0.05)
    .modulate(osc(60, 0.05, 0).kaleid(100))
  	.scrollX(-0.2)
  )
  .out()
```
