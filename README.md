# Lab 08 - Creative Coding with Hydra
Let's explore creative coding and "live coding"! In this lab we'll be using [Hydra](https://hydra.ojack.xyz/), a tool for live coding interesting visuals. Hydra has a lot of support for new users, but it's best to learn by starting to play around. In addition to the [Hydra Documentation](https://hydra.ojack.xyz/docs/), consider checking out these resources:

- What is modulation? https://hydra-book.glitch.me/#/modulation
- How to use textures? https://hydra-book.glitch.me/#/textures  
- A short starter walkthrough: https://www.clipsoundandmusic.uk/hydra-tutorial-a-beginners-guide-to-live-coding-visuals/

All credit to the creator of hydra, [olivia](https://ojack.xyz/), and the hydra community.

If you're interested in learning more about live coding, check out [this guide](https://static.livecodingbook.toplap.org/books/livecoding.pdf).

lecture notes: https://tinyurl.com/penn-lets-get-creative
three.js docs: https://threejs.org/docs/index.html#manual/en/introduction/Creating-a-scene
         
## Lab Solution:

### 1. Puzzle 1: You're getting sleepy

[Link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEFzaGFwZSg5OSUyQyUyMDAuNSUyQyUyMDApLmNvbG9yKDEuMCUyQzAuMCUyQzEuMCkubXVsdChvc2MoNTAlMkMtMC4xJTJDMC4wKS5rYWxlaWQoNTApKS5zY3JvbGxYKCU1Qi0wLjIlMkMwLjIlNUQuc21vb3RoKCkpLm91dChvMCklMEElMEFyZW5kZXIobzApJTBBJTBB)

![d2765d83f53a79102bbee596dc137abf](https://github.com/user-attachments/assets/a5f6f0da-5ca7-4066-9ceb-8851c2a14071)

### 2. Puzzle 2: Dancing Squares

[Link](https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEElMEFjb25zdCUyMFRIUkVFJTIwJTNEJTIwYXdhaXQlMjBpbXBvcnQoJTIyaHR0cHMlM0ElMkYlMkZ1bnBrZy5jb20lMkZ0aHJlZSU0MDAuMTYzLjAlMkZidWlsZCUyRnRocmVlLm1vZHVsZS5qcyUyMiklMEElMEFzY2VuZSUyMCUzRCUyMG5ldyUyMFRIUkVFLlNjZW5lKCklMEFjYW1lcmElMjAlM0QlMjBuZXclMjBUSFJFRS5QZXJzcGVjdGl2ZUNhbWVyYSg3NSUyQyUyMHdpbmRvdy5pbm5lcldpZHRoJTIwJTJGJTIwd2luZG93LmlubmVySGVpZ2h0JTJDJTIwMC4xJTJDJTIwMTAwMCklMEElMEFyZW5kZXJlciUyMCUzRCUyMG5ldyUyMFRIUkVFLldlYkdMUmVuZGVyZXIoKSUwQXJlbmRlcmVyLnNldFNpemUod2lkdGglMkMlMjBoZWlnaHQpJTBBZ2VvbWV0cnklMjAlM0QlMjBuZXclMjBUSFJFRS5Cb3hHZW9tZXRyeSgpJTBBbWF0ZXJpYWwlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoQmFzaWNNYXRlcmlhbCglN0Jjb2xvciUzQSUyMDB4MDBmZjAwJTdEKSUwQWN1YmUlMjAlM0QlMjBuZXclMjBUSFJFRS5NZXNoKGdlb21ldHJ5JTJDJTIwbWF0ZXJpYWwpJTNCJTBBJTBBc2NlbmUuYWRkKGN1YmUpJTBBY2FtZXJhLnBvc2l0aW9uLnolMjAlM0QlMjAxLjUlMEElMEElMkYlMkYlMjAndXBkYXRlJyUyMGlzJTIwYSUyMHJlc2VydmVkJTIwZnVuY3Rpb24lMjB0aGF0JTIwd2lsbCUyMGJlJTIwcnVuJTIwZXZlcnklMjB0aW1lJTIwdGhlJTIwbWFpbiUyMGh5ZHJhJTIwcmVuZGVyaW5nJTIwY29udGV4dCUyMGlzJTIwdXBkYXRlZCUwQXVwZGF0ZSUyMCUzRCUyMCgpJTIwJTNEJTNFJTIwJTdCJTBBJTIwJTIwY3ViZS5yb3RhdGlvbi55JTIwJTJCJTNEJTIwMC4wNSUzQiUwQSUyMCUyMGN1YmUucm90YXRpb24ueCUyMCUyQiUzRCUyMDAuMDUlM0IlMEElMjAlMjByZW5kZXJlci5yZW5kZXIoJTIwc2NlbmUlMkMlMjBjYW1lcmElMjApJTNCJTBBJTdEJTBBJTBBczAuaW5pdCglN0IlMjBzcmMlM0ElMjByZW5kZXJlci5kb21FbGVtZW50JTIwJTdEKSUwQSUwQXNyYyhzMCkucmVwZWF0KDMuMCUyQyUyMDMuMCUyQyUyMDAuMCUyQyUyMDAuMCklMEElMjAlMjAub3V0KCklMEE%3D)
[![Image from Gyazo](https://i.gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51.gif)](https://gyazo.com/95ace79f6d2ca24f563a6a79fdcc4f51)
     
### 3. Your own cool effect!

[Link](https://hydra.ojack.xyz/?sketch_id=cz0dcC84hG6IOovv)
  
# Submission:
- Create a pull request against this repository
- In your readme, add links to your solutions for each of the puzzles, three links total
- Profit
