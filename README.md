# Lab 08 - Creative Coding with Hydra

## Submission (Charles Wang)

Puzzle 1: [link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwYWN6dyUwQW9zYyg2MCUyQyUyMC0wLjEpLmNvbG9yKDElMkMlMjAwJTJDJTIwMSkua2FsZWlkKDUwKS5tYXNrKHNoYXBlKDUwJTJDJTIwMC41KSkuc2Nyb2xsWCglNUItMC4yJTJDJTIwMC4yJTVELnNtb290aCgpKS5vdXQobzApJTBB)

```
// aczw
osc(60, -0.1).color(1, 0, 1).kaleid(50).mask(shape(50, 0.5)).scrollX([-0.2, 0.2].smooth()).out(o0)
```

Puzzle 2: [link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEElMEFjb25zdCUyMFRIUkVFJTIwJTNEJTIwYXdhaXQlMjBpbXBvcnQoJTIyaHR0cHMlM0ElMkYlMkZ1bnBrZy5jb20lMkZ0aHJlZSU0MDAuMTYzLjAlMkZidWlsZCUyRnRocmVlLm1vZHVsZS5qcyUyMiklMEElMEFzY2VuZSUyMCUzRCUyMG5ldyUyMFRIUkVFLlNjZW5lKCklMEFjYW1lcmElMjAlM0QlMjBuZXclMjBUSFJFRS5QZXJzcGVjdGl2ZUNhbWVyYSg3NSUyQyUyMHdpbmRvdy5pbm5lcldpZHRoJTIwJTJGJTIwd2luZG93LmlubmVySGVpZ2h0JTJDJTIwMC4xJTJDJTIwMTAwMCklMEElMEFyZW5kZXJlciUyMCUzRCUyMG5ldyUyMFRIUkVFLldlYkdMUmVuZGVyZXIoKSUwQXJlbmRlcmVyLnNldFNpemUod2lkdGglMkMlMjBoZWlnaHQpJTBBZ2VvbWV0cnklMjAlM0QlMjBuZXclMjBUSFJFRS5Cb3hHZW9tZXRyeSgpJTBBbWF0ZXJpYWwlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoQmFzaWNNYXRlcmlhbCglN0Jjb2xvciUzQSUyMDB4MDBmZjAwJTdEKSUwQWN1YmUlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoKGdlb21ldHJ5JTJDJTIwbWF0ZXJpYWwpJTNCJTBBc2NlbmUuYWRkKGN1YmUpJTBBY2FtZXJhLnBvc2l0aW9uLnolMjAlM0QlMjAxLjUlMEElMEFsZXQlMjB0aW1lJTIwJTNEJTIwMCUzQiUwQSUwQSUyRiUyRiUyMCd1cGRhdGUnJTIwaXMlMjBhJTIwcmVzZXJ2ZWQlMjBmdW5jdGlvbiUyMHRoYXQlMjB3aWxsJTIwYmUlMjBydW4lMjBldmVyeSUyMHRpbWUlMjB0aGUlMjBtYWluJTIwaHlkcmElMjByZW5kZXJpbmclMjBjb250ZXh0JTIwaXMlMjB1cGRhdGVkJTBBdXBkYXRlJTIwJTNEJTIwKCklMjAlM0QlM0UlMjAlN0IlMEElMjAlMjBjdWJlLnJvdGF0aW9uLnklMjAlMkIlM0QlMjAwLjAxJTNCJTBBJTIwJTIwY3ViZS5yb3RhdGlvbi54JTIwJTJCJTNEJTIwMC4wMSUyMColMjBNYXRoLnNpbih0aW1lKSUzQiUwQSUyMCUyMHJlbmRlcmVyLnJlbmRlciglMjBzY2VuZSUyQyUyMGNhbWVyYSUyMCklM0IlMEElMjAlMjB0aW1lJTIwJTJCJTNEJTIwMC4wMSUzQiUwQSU3RCUwQSUwQXMwLmluaXQoJTdCJTIwc3JjJTNBJTIwcmVuZGVyZXIuZG9tRWxlbWVudCUyMCU3RCklMEElMEFzcmMoczApLnJlcGVhdCgzJTJDJTIwMyklMEElMjAlMjAub3V0KCklMEE%3D)

```
// licensed with CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/

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

let time = 0;

// 'update' is a reserved function that will be run every time the main hydra rendering context is updated
update = () => {
  cube.rotation.y += 0.01;
  cube.rotation.x += 0.01 * Math.sin(time);
  renderer.render( scene, camera );
  time += 0.01;
}

s0.init({ src: renderer.domElement })

src(s0).repeat(3, 3)
  .out()
```

Puzzle 3: [link](https://hydra.ojack.xyz/?code=b3NjKDYlMkMlMjAxJTJDJTIwNSklMEElMjAlMjAuc3ViKG5vaXNlKDAuNyUyQyUyMDEpKSUwQSUyMCUyMC5yb3RhdGUoKCklMjAlM0QlM0UlMjB0aW1lJTIwJTI1JTIwMzYwKSUwQSUyMCUyMC5waXhlbGF0ZSgzMCUyQyUyMCU1QjUlMkMlMjAxMCUyQyUyMDE1JTJDJTIwMjAlNUQuZmFzdChNYXRoLlBJKSklMEElMjAlMjAubW9kdWxhdGVQaXhlbGF0ZShvc2MoNCklMkMlMjA0JTJDJTIwJTVCMSUyQyUyMDIwJTJDJTIwLTEwJTJDJTIwNSUyQyUyMDEwMCUyQyUyMC0xNyUyQyUyMDY5JTJDJTIwLTQyMCUyQyUyMDEzMzclNUQuZmFzdCgyKSklMEElMjAlMjAub3V0KG8wKQ%3D%3D)

```
osc(6, 1, 5)
  .sub(noise(0.7, 1))
  .rotate(() => time % 360)
  .pixelate(30, [5, 10, 15, 20].fast(Math.PI))
  .modulatePixelate(osc(4), 4, [1, 20, -10, 5, 100, -17, 69, -420, 1337].fast(2))
  .out(o0)
```
