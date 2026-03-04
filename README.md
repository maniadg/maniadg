# George Maniadakis

**BSc Computer Science, Year 3 — Newcastle University**

I build computational physics tools — interactive simulators and visualisers that make the underlying mathematics tangible. My work sits at the intersection of scientific computing, numerical methods, and physics and I am currently applying for master's programmes in quantum computing and scientific computing.

---

## Currently Working On

### Dissertation — *Alternative Guidance Schemes in Pilot-Wave Theory*

Investigating a Green's function-based alternative to the canonical de Broglie–Bohm guidance equation, inspired by the Many Interacting Worlds framework. The standard Bohmian guidance velocity is not uniquely determined by the Schrödinger equation — any divergence-free term may be added to the probability current without violating the continuity equation. This project constructs and numerically simulates one such alternative: a nonlocal, curl-free velocity field derived via a Green's function construction analogous to Coulomb's law.

The key consequence is the absence of vortical structure near nodal regions — a primary driver of relaxation to quantum equilibrium in standard pilot-wave theory. The study investigates whether this suppression of vorticity leads to qualitatively different quantum nonequilibrium behaviour, quantified via L1, L2, and subquantum H-function diagnostics.

Implemented in two spatial dimensions and using something like the 2D isotropic harmonic oscillator below as a benchmark system — it provides exact analytic wavefunctions for clean validation against canonical dBB dynamics.

> *Code and writeup will be pushed here upon completion (May 2026)*

---

## Projects

### [WaveNode](https://github.com/maniadg/WaveNode) &nbsp;·&nbsp; *Julia, GLMakie*
> Real-time visualiser for quantum superposition states of the 2D isotropic harmonic oscillator

Built around the angular (polar) eigenbasis of the 2D isotropic quantum harmonic oscillator in dimensionless units. Time evolution is exact — each eigenstate accumulates a Schrödinger phase factor, no PDE stepping required. The result is a live, interactive window into quantum interference and vortex dynamics.

**What it does:**
- Renders Born density |ψ|² and iso-probability contours in real time across a full 2π period
- Detects quantised phase vortices (topological charges q = ±1) via discrete winding number on grid plaquettes
- Superposition states are user-defined or randomly generated with controllable energy truncation and seed
- States persist between sessions; ships with a curated set including rotationally symmetric and high-vortex configurations
- Physics cross-verified against an independent Mathematica implementation to 6 decimal places

|   |  |
| ------------- | ------------- |
| ![WaveNode — six-lobe superposition with phase vortices](https://raw.githubusercontent.com/maniadg/WaveNode/main/assets/wavenode_preview.png) |  ![WaveNode — superposition state](https://raw.githubusercontent.com/maniadg/WaveNode/main/assets/wavenode_preview_spider.png)

---

### [OrbitForge](https://github.com/maniadg/OrbitForge) &nbsp;·&nbsp; *Julia, GLMakie*
> Interactive N-body simulator for hierarchical triple systems with real-time Kozai-Lidov diagnostics

Integrates three-body gravitational systems directly — no secular averaging, no approximations. The focus is the Kozai-Lidov (KL) mechanism: a secular exchange between the inner binary's eccentricity and mutual inclination driven by a distant third body. Astrophysically, KL oscillations drive tidal circularisation of stellar binaries, asteroid delivery to Earth-crossing orbits, and compact binary mergers detectable by LIGO.

**What it does:**
- Reproduces Kozai (1962) Figure 1 from first principles via a 19-point inclination parameter sweep
- Implements the Eccentric Kozai-Lidov (EKL) octupole correction, active when m₁ ≠ m₂ or e_out > 0
- Live Poincaré section sampled at outer ascending node crossings — distinguishes regular from chaotic orbits in real time
- Lyapunov exponent via Benettin (1980) renormalisation with a shadow trajectory offset by δr₀ = 10⁻⁸
- Mardling-Aarseth stability boundary tracked live in (e_out, a_out/a_in) space
- Three integrators: Velocity-Verlet KDK (2nd order symplectic), Yoshida4 (4th order symplectic), RK4 (non-symplectic) — energy drift difference directly observable

![OrbitForge - example simulation panel with no control panel visible](https://raw.githubusercontent.com/maniadg/OrbitForge/main/assets/preview.png)

---

## Skills

**Languages**

| Language | |
|---|---|
| **Julia** | Scientific simulation, high-performance numerical code, GLMakie visualisation |
| **Python** | data analysis, scripting, scientific computing |
| **Java** | Object-oriented design, algorithms and data structures |
| **R** | Statistical analysis |
| **SQL** | Relational databases and querying |
| **Bash / Linux** | Scripting, automation, HPC-style workflows |
| **LaTeX** | Scientific writing and typesetting |

**Areas**
- Numerical methods: symplectic integration, ODE solvers, Green's function methods, basis expansions
- Quantum mechanics: pilot-wave theory, eigenbasis time evolution, phase space, vortex dynamics, quantum nonequilibrium
- Celestial mechanics: N-body dynamics, osculating orbital elements, secular perturbation theory
- Scientific visualisation: real-time interactive rendering, observable-driven UI architecture

---

📧 [c3034838@newcastle.ac.uk](mailto:c3034838@newcastle.ac.uk)
