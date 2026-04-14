# Ram Chandra Giri

MSc Physics | Computational Physics (PhD aspirant)  
Nepal

---

## About

I am a physics graduate currently teaching at college level and systematically preparing for PhD applications in **Computational Physics**.

This GitHub documents my learning and projects in:

- Numerical methods for physics
- Computational modeling and simulation
- Scientific Python

I am building a strong foundation in computation alongside physics.

---

## Current Focus

- Python for scientific computing
- Numerical solutions of physical systems
- Physics-inspired simulation projects
- Legacy code modernization and performance benchmarking

---

## Portfolio Projects

[Driven LCR-Series Circuit Modernization](https://github.com/rcgiri-physics/LCR-Circuit-Modernization)

A structural migration of a 2023 procedural Fortran 90 dissertation into a high-performance, vectorized Python framework.

- Numerical Validation: Verified the custom RK4 algorithm against SciPy (`scipy.integrate.solve_ivp`), achieving a maximum residual error of $< 10^{-7}$.

- Legacy Cross-Validation: Mathematically verified transient boundary conditions by achieving a 100% trace overlap between modern Python outputs and legacy Fortran data.

- Performance Auditing: Conducted 1,000,000-step execution benchmarks to analyze the computational overhead of Python interpreter loops versus compiled Fortran for sequential differential equations.

- Phase Space Analysis: Visualized topological attractor dynamics to map energy dissipation and limit cycles across complex damping constraints.

[Projectile Motion: From Vacuum to Quadratic Drag](https://github.com/rcgiri-physics/projectile-simulation)

A research-validated study on dissipative systems using high-order numerical integration.

- Version 2.1 Milestone: Implemented a Numerical Audit & Residual Analysis framework.

- Validation: Cross-verified the custom engine against the industry-standard scipy.integrate.solve_ivp (RK45) benchmark.

- Precision: Achieved 99.98% accuracy with a maximum vertical deviation of $\approx 5.31 \times 10^{-3}$ meters over non-linear trajectories.

- Architecture: Utilized a vectorized state-space representation in NumPy, optimizing for $O(\Delta t^4)$ global error scaling.

---

## 2026 Research Roadmap

| Month | Project Focus | Status |
| :--- | :--- | :--- |
| **Jan** | Projectile v1.0 (Euler/Pure Python) | **Completed** |
| **Feb** | Projectile v2.1: RK4 Engine, Vectorization, & SciPy Validation | **Completed** |
| **Apr** | LCR_Modernization: Vectorization, Benchmarking & Phase Space mapping | **Completed** |
| **Apr** | Chaotic 3-Body Dynamics: Orbital Stability & Symplectic Systems | **In Progress** |
| **May/June** | **TBD** | **Planning** |

---

> This profile will be updated progressively as my work develops.
