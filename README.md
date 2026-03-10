# Fluid Glass + Dithering

A standalone WebGL2 demo combining a fluid glass simulation with a 4x4 Bayer ordered dithering post-process effect. No build tools or dependencies required — just one HTML file.

![Fluid Glass Dithering](https://img.shields.io/badge/WebGL2-Standalone-blue)

## Demo

**[Live Demo](https://glaseagle.github.io/fluidglass-dither/)**

Or open `index.html` in any modern browser, or serve it locally:

```bash
npx serve -s .
```

## Features

- **Fluid Simulation** — Navier-Stokes equations drive a real-time velocity/pressure field
- **Reaction-Diffusion** — Gray-Scott model generates organic glass blob shapes from display text
- **Glass Rendering** — Snell's law refraction, Fresnel reflection, and chromatic aberration
- **Animated Background** — Clock-driven colored circles with parallax from mouse/gyroscope
- **Dithering Post-Process** — 4x4 Bayer ordered dithering with pixelation, grayscale, invert, and color tint
- **Interactive** — Mouse and touch input disturb the fluid simulation
- **Control Panel** — Full real-time control over every parameter:
  - Editable display text (supports `{{time}}` and `{{date}}` placeholders)
  - Font size
  - Reaction-diffusion feed, kill, iteration count
  - Glass color, shadow, brightness
  - Background and circle colors
  - Dithering grid size, pixel ratio, grayscale, invert, tint color/strength
- **Presets** — Default, Cosmos Black, Sticky Pink, Cozzy Blue, Retro Dither, Newspaper
- **Save/Load** — Save your settings as the new default via localStorage

## Controls

| Input | Action |
|-------|--------|
| Mouse move | Parallax + fluid disturbance |
| Touch drag | Fluid disturbance (mobile) |
| Device tilt | Parallax (mobile gyroscope) |
| Settings panel | Adjust all parameters in real-time |

## Sources

This project combines and ports two open-source projects into a single standalone vanilla WebGL2 file:

| Project | Author | Description | License |
|---------|--------|-------------|---------|
| [Fluid Glass](https://github.com/chiuhans111/fluidglass) | [@chiuhans111](https://github.com/chiuhans111) | Liquid fluid glass WebGL demo using OGL + Vue | — |
| [Dithering Shader](https://github.com/niccolofanton/dithering-shader) | [@niccolofanton](https://github.com/niccolofanton) | Dithering post-processing effect for Three.js | MIT |

## License

MIT
