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

- **Hamiltonian & Symplectic Dynamics:** Implementing energy-conserving integrators for long-term orbital stability.
- **Chaos & Nonlinear Dynamics:** Quantifying sensitivity to initial conditions through Lyapunov divergence and bifurcation mapping.
- **Scientific Python:** Vectorized state-space modeling and performance benchmarking of numerical engines.

---

## Portfolio Projects

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
| **May/June**| **Lagrangian Mechanics: Double Pendulum & Bifurcation Analysis** | **Next Up**|

---

> This profile is updated progressively as my research and computational framework develop.
