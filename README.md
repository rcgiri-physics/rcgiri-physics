# Ram Chandra Giri

MSc Physics | Computational Physics (PhD aspirant)  
Nepal

---

## About

I am an MSc Physics graduate and educator specializing in the **numerical modeling of complex physical systems**. My work focuses on bridging the gap between theoretical frameworks and high-performance computation, with a specific emphasis on the long-term stability of Hamiltonian and Lagrangian systems.

This portfolio documents my research and implementations in:
- **Classical & Nonlinear Dynamics:** Symplectic integrators, chaos theory (3-Body problem), and strange attractors.
- **Computational Methods:** High-order ODE solvers (RK4/Verlet), vectorized state-space modeling, and numerical linear algebra.
- **Performance Engineering:** Scientific Python benchmarking and legacy code modernization (Fortran-to-Python migration).

I am systematically building a rigorous foundation for a PhD in **Computational Physics**.

---

## Current Focus

- **Atmospheric Chaos:** Implementing the Lorenz system to study the topology of strange attractors and the "Butterfly Effect."
- **Bifurcation Theory:** Identifying period-doubling routes to chaos and quantifying sensitivity to initial conditions.
- **Matrix Mechanics (Coming June):** Transitioning to computational linear algebra, eigenvalue problems, and normal mode analysis.
- **Symplectic Integration:** Developing energy-conserving numerical engines for N-body and oscillating systems.

---

## Portfolio Projects

### [Lagrangian Mechanics: The Double Pendulum](https://github.com/rcgiri-physics/double-pendulum-simulation)
A deep dive into multi-degree-of-freedom systems and the onset of chaos through Lagrangian mechanics.

- **Euler-Lagrange Derivation:** Formulated the non-linear equations of motion for a coupled pendulum system using generalized coordinates.
- **Phase Space Mapping:** Visualized the transition from periodic motion to chaotic flipping using state-space trajectories.

### [3-Body Laboratory: Symplectic Physics Engine](https://github.com/rcgiri-physics/three-body-simulation)
A high-precision study of gravitational stability, transition to chaos, and long-term orbital conservation.

- **Symplectic Engineering:** Developed a custom Velocity-Verlet (Leapfrog) engine in Python to eliminate numerical energy dissipation, maintaining a relative Hamiltonian error of $\sim 10^{-9}$.
- **Chaos Quantification:** Identified a critical velocity perturbation threshold ($\delta \approx 0.5$) for stellar ejection using Lyapunov divergence mapping.
- **Astronomical Validation:** Verified engine stability through a 12-year simulation of the Sun-Earth-Jupiter system using Astronomical Units and Solar Masses ($G = 4\pi^2$).
- **Visualization:** Authored a cinematic rendering suite to visualize "Butterfly Effect" divergence and total system collapse.

### [Driven LCR-Series Circuit Modernization](https://github.com/rcgiri-physics/LCR-Circuit-Modernization)
A structural migration of a 2023 procedural Fortran 90 dissertation into a high-performance, vectorized Python framework.

- **Numerical Validation:** Verified custom RK4 algorithms against SciPy, achieving a maximum residual error of $< 10^{-7}$.
- **Legacy Cross-Validation:** Achieved 100% trace overlap between modern Python outputs and legacy Fortran data.
- **Performance Auditing:** Benchmarked Python interpreter loops versus compiled Fortran for 1,000,000-step execution cycles.

### [Projectile Motion: From Vacuum to Quadratic Drag](https://github.com/rcgiri-physics/projectile-simulation)
A research-validated study on dissipative systems using high-order numerical integration.

- **Precision:** Achieved 99.98% accuracy with a maximum vertical deviation of $\approx 5.31 \times 10^{-3}$ meters over non-linear trajectories.
- **Architecture:** Utilized a vectorized state-space representation in NumPy, optimizing for $O(\Delta t^4)$ global error scaling.

---

## 2026 Research Roadmap

| Month | Project Focus | Status |
| :--- | :--- | :--- |
| **Jan** | Projectile v1.0 (Euler/Pure Python) | **Completed** |
| **Feb** | Projectile v2.1: RK4 Engine, Vectorization, & SciPy Validation | **Completed** |
| **Apr** | LCR_Modernization: Vectorization, Benchmarking & Phase Space mapping | **Completed** |
| **Apr** | Chaotic 3-Body Dynamics: Symplectic Systems & Ejection Thresholds | **Completed**|
| **May**| **Lagrangian Mechanics: Double Pendulum** | **Completed**|
| **May** | **Lorenz Attractor: Strange Attractors & Chaos Mapping** | **In Progress** |
| **June** | **Computational Linear Algebra: Matrix Mechanics & Normal Modes** | **Next Up** |

---

> "Physics is the only profession in which prophecy is not only allowed but required." — This profile tracks my progress in mastering those prophecies through code.
