[![Crates.io](https://img.shields.io/crates/v/macroquad-canvas?style=flat)](https://crates.io/crates/macroquad-canvas)
[![Lib.rs](https://img.shields.io/crates/v/macroquad-canvas?color=%2384f&label=lib.rs)](https://lib.rs/crates/macroquad-canvas)
[![docs.rs](https://img.shields.io/docsrs/macroquad-canvas?style=flat)](https://docs.rs/macroquad-canvas/0.3.2/macroquad_canvas/)
[![License](https://img.shields.io/crates/l/macroquad-canvas)](https://gitlab.com/alexmozaidze/macroquad-canvas/-/blob/main/LICENSE)

# Macroquad Canvas Pixel Perfect

*This is a fork of [Macroquad Canvas]()*

A library that allows for maintaining a certain aspect ratio within your [Macroquad](https://github.com/not-fl3/macroquad) games while keeping crisp pixel perfect detail. 

## How To Use

To use this library, import `Canvas2D`

```rust
use macroquad_canvas::Canvas2D;
```

Then simply create the canvas

```rust
let canvas = Canvas2D::new(800_f32, 600_f32);
```

And here's how to draw the canvas

```rust
loop {
    set_camera(&canvas.camera);

    // Draw inside canvas...

    set_default_camera();

    canvas.draw();

    next_frame().await
}
```
