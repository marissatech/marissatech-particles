# MarissaTech Particles

A tiny WebGL2 particle toy for the browser.

It runs the particle physics on the GPU, so you can push it way past what a normal JavaScript loop would handle. Drag around, paint particles, switch counts, and see how far your device wants to go.

[Live demo](https://marissatech.github.io/marissatech-particles/)

## What it does

* GPU particle simulation with WebGL2 transform feedback
* Adjustable particle counts from `2^15` up to `2^21`
* Draw mode for painting particles into the scene
* Gravity and repel interactions
* Trails, size, and physics speed controls
* Works on desktop and mobile browsers that support WebGL2

## Controls

Drag or touch the canvas to interact with the particles.

Use the bottom panel to change particle count, tool mode, gravity, trail amount, particle size, and physics speed.

Higher particle counts look great, but `2^21` is intentionally a stress test. Some phones and older laptops may prefer a lower setting.

## Running locally

No build step. No dependencies.

Just open:

```txt
index.html
```

Or serve the folder locally:

```bash
python3 -m http.server
```

Then visit:

```txt
http://localhost:8000
```

## Notes

The simulation keeps position and velocity data on the GPU. Each frame updates the particle buffer using transform feedback, then renders the points with additive blending.

That keeps the CPU mostly out of the way, which is what makes the large particle counts possible.

## Author

Made by MarissaTech.
