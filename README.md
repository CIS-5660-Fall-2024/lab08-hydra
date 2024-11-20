# Lab 08 - Creative Coding with Hydra
Let's explore creative coding and "live coding"! In this lab we'll be using [Hydra](https://hydra.ojack.xyz/), a tool for live coding interesting visuals. Hydra has a lot of support for new users, but it's best to learn by starting to play around. In addition to the [Hydra Documentation](https://hydra.ojack.xyz/docs/), consider checking out these resources:

- What is modulation? https://hydra-book.glitch.me/#/modulation
- How to use textures? https://hydra-book.glitch.me/#/textures  
- A short starter walkthrough: https://www.clipsoundandmusic.uk/hydra-tutorial-a-beginners-guide-to-live-coding-visuals/

All credit to the creator of hydra, [olivia](https://ojack.xyz/), and the hydra community.

If you're interested in learning more about live coding, check out [this guide](https://static.livecodingbook.toplap.org/books/livecoding.pdf).
         
## Lab Puzzles:
The goal of each puzzle will be to replicate the look of each puzzle’s image by exploring the hydra api.

### 1. Puzzle 1: You're getting sleepy

![d2765d83f53a79102bbee596dc137abf](https://github.com/user-attachments/assets/a5f6f0da-5ca7-4066-9ceb-8851c2a14071)

   * Starting with [this code](https://hydra.ojack.xyz/?sketch_id=mwVfjOO8YNtqODRt) as a base, replicate the above animation.

osc(0,0,0).color(0,0,0)
  .layer(osc(25,-0.1,0).kaleid(50).color(1,0,1).scrollX([-0.1,0.1].smooth())
         .mask(shape(999).scale(1.5,1.5,1.5).scrollX([-0.1,0.1].smooth()), 1, 1))

  .out(o0)

### 2. Puzzle 2: Dancing Squares
[![Image from Gyazo](https://i.gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51.gif)](https://gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51)

   * Starting with [this code](https://hydra.ojack.xyz/?sketch_id=FpvaIGZZzA87TUA4) as a base, replicate the above animation.

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
  cube.rotation.y += 0.01;
  cube.rotation.x += 0.01;
  renderer.render( scene, camera );
}

s0.init({ src: renderer.domElement })

src(s0).repeat(3.0, 3.0, 0.0, 0.0)
  .out()

     
### 3. Your own cool effect!

   * Create your own shader effect! If you need a starting point, try starting with the "random" button at the top of the hydra page.
  
# Submission:
- Create a pull request against this repository
- In your readme, add links to your solutions for each of the puzzles, three links total
- Profit
