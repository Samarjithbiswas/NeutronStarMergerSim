# GW170817 — Binary Neutron Star Merger Simulation

An interactive, browser-based simulation of the GW170817 binary neutron star
merger: 3D inspiral visualization, real-time gravitational-wave strain, chirp
audio, and a live spectrogram. Single HTML file, WebGL, no build step.

**Live demo:** [samarjithbiswas.com/gw170817](https://samarjithbiswas.com/gw170817/)

## The physics that is real

The inspiral is equation-driven at every frame, not keyframed animation:

- **Orbital decay** by Peters' equations with 2.5 post-Newtonian corrections,
  integrated with 4th-order Runge-Kutta
- **Gravitational-wave strain** from the quadrupole formula with the 0.5PN
  amplitude correction
- **Tidal deformability** with the GW170817 combined dimensionless
  deformability (Λ̃ ≈ 300), following Flanagan & Hinderer (2008)
- **Source parameters** taken directly from Abbott et al., *Phys. Rev. X* **9**,
  011001 (2019); PN flux per Blanchet (2006); constants per CODATA
- The **chirp audio** maps the actual GW frequency evolution to sound, and the
  spectrogram is computed live from the strain

## The part that is visual approximation, stated plainly

The post-merger phase (kilonova ejecta, relativistic jets, remnant collapse) is
a visual approximation. That physics requires full numerical relativity with
neutrino transport and GRMHD on supercomputers; no single-file WebGL page is
doing that. The boundary between computed and illustrated is deliberately kept
visible.

## Run it

Open `index.html` in a browser, or serve the folder with any static server.
No dependencies, no build.

## License

MIT.
