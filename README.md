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

[my link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEElMEFvc2MoMCUyQzAlMkMwKS5jb2xvcigwJTJDMCUyQzApJTBBJTIwJTIwLmxheWVyKG9zYygyNSUyQy0wLjElMkMwKS5rYWxlaWQoNTApLmNvbG9yKDElMkMwJTJDMSkuc2Nyb2xsWCglNUItMC4xJTJDMC4xJTVELnNtb290aCgpKSUwQSUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMCUyMC5tYXNrKHNoYXBlKDk5OSkuc2NhbGUoMS41JTJDMS41JTJDMS41KS5zY3JvbGxYKCU1Qi0wLjElMkMwLjElNUQuc21vb3RoKCkpJTJDJTIwMSUyQyUyMDEpKSUwQSUwQSUyMCUyMC5vdXQobzApJTBBJTBB)

osc(0,0,0).color(0,0,0)
  .layer(osc(25,-0.1,0).kaleid(50).color(1,0,1).scrollX([-0.1,0.1].smooth())
         .mask(shape(999).scale(1.5,1.5,1.5).scrollX([-0.1,0.1].smooth()), 1, 1))

  .out(o0)

### 2. Puzzle 2: Dancing Squares
[![Image from Gyazo](https://i.gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51.gif)](https://gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51)

   * Starting with [this code](https://hydra.ojack.xyz/?sketch_id=FpvaIGZZzA87TUA4) as a base, replicate the above animation.

[my link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEElMEFjb25zdCUyMFRIUkVFJTIwJTNEJTIwYXdhaXQlMjBpbXBvcnQoJTIyaHR0cHMlM0ElMkYlMkZ1bnBrZy5jb20lMkZ0aHJlZSU0MDAuMTYzLjAlMkZidWlsZCUyRnRocmVlLm1vZHVsZS5qcyUyMiklMEElMEFzY2VuZSUyMCUzRCUyMG5ldyUyMFRIUkVFLlNjZW5lKCklMEFjYW1lcmElMjAlM0QlMjBuZXclMjBUSFJFRS5QZXJzcGVjdGl2ZUNhbWVyYSg3NSUyQyUyMHdpbmRvdy5pbm5lcldpZHRoJTIwJTJGJTIwd2luZG93LmlubmVySGVpZ2h0JTJDJTIwMC4xJTJDJTIwMTAwMCklMEElMEFyZW5kZXJlciUyMCUzRCUyMG5ldyUyMFRIUkVFLldlYkdMUmVuZGVyZXIoKSUwQXJlbmRlcmVyLnNldFNpemUod2lkdGglMkMlMjBoZWlnaHQpJTBBZ2VvbWV0cnklMjAlM0QlMjBuZXclMjBUSFJFRS5Cb3hHZW9tZXRyeSgpJTBBbWF0ZXJpYWwlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoQmFzaWNNYXRlcmlhbCglN0Jjb2xvciUzQSUyMDB4MDBmZjAwJTdEKSUwQWN1YmUlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoKGdlb21ldHJ5JTJDJTIwbWF0ZXJpYWwpJTNCJTBBc2NlbmUuYWRkKGN1YmUpJTBBY2FtZXJhLnBvc2l0aW9uLnolMjAlM0QlMjAxLjUlMEElMEElMkYlMkYlMjAndXBkYXRlJyUyMGlzJTIwYSUyMHJlc2VydmVkJTIwZnVuY3Rpb24lMjB0aGF0JTIwd2lsbCUyMGJlJTIwcnVuJTIwZXZlcnklMjB0aW1lJTIwdGhlJTIwbWFpbiUyMGh5ZHJhJTIwcmVuZGVyaW5nJTIwY29udGV4dCUyMGlzJTIwdXBkYXRlZCUwQXVwZGF0ZSUyMCUzRCUyMCgpJTIwJTNEJTNFJTIwJTdCJTBBJTIwJTIwY3ViZS5yb3RhdGlvbi55JTIwJTJCJTNEJTIwMC4wMSUzQiUwQSUyMCUyMGN1YmUucm90YXRpb24ueCUyMCUyQiUzRCUyMDAuMDElM0IlMEElMjAlMjByZW5kZXJlci5yZW5kZXIoJTIwc2NlbmUlMkMlMjBjYW1lcmElMjApJTNCJTBBJTdEJTBBJTBBczAuaW5pdCglN0IlMjBzcmMlM0ElMjByZW5kZXJlci5kb21FbGVtZW50JTIwJTdEKSUwQSUwQXNyYyhzMCkucmVwZWF0KDMuMCUyQyUyMDMuMCUyQyUyMDAuMCUyQyUyMDAuMCklMEElMjAlMjAub3V0KCk%3D)

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

[my link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwYnklMjBDaHJpc3RpbmElMjBRaXUlMEElMEFzMC5pbml0Q2FtKCklMEElMEFzcmMoczApLmthbGVpZCgoKSUzRCUzRTYlMkJNYXRoLnNpbih0aW1lKSo1KS5jb2xvcmFtYSglNUIwLjAwNSUyQzAuMzMlMkMwLjY2JTJDMS4wJTVELmZhc3QoMSkpLm91dChvMCk%3D)

s0.initCam()
src(s0).pixelate(20,20).kaleid(()=>6+Math.sin(time)*4).colorama([0.005,0.33,0.66,1.0].fast(0.125)).out(o0)
  
# Submission:
- Create a pull request against this repository
- In your readme, add links to your solutions for each of the puzzles, three links total
- Profit
