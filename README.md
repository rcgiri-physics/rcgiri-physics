# Ram Chandra Giri

MSc Physics | Computational Physics (PhD aspirant)
Nepal

---

## About

Physics educator and computational researcher focusing on the explicit numerical modeling of non-linear dynamical systems. My work evaluates the long-term phase-space stability of Hamiltonian, Lagrangian, and dissipative chaotic models.

I treat my code repositories as formal numerical laboratories. My methodology prioritizes mathematical rigor, strict physical conservation proofs, and custom algorithmic execution over pre-built library wrappers. I am systematically building a technical and mathematical foundation for a PhD in Computational Physics and Nonlinear Dynamics.

---

## Portfolio Projects

### [Lorenz Attractor Simulation: Strange Attractors & Deterministic Chaos](https://github.com/rcgiri-physics/lorenz-attractor-simulation)
A computational framework designed to model, visualize, and analyze deterministic chaos within the three-dimensional, non-linear atmospheric flow model derived by Edward Lorenz.

$$
\frac{dx}{dt} = \sigma(y - x), \quad \frac{dy}{dt} = x(\rho - z) - y, \quad \frac{dz}{dt} = xy - \beta z
$$

* **Numerical Engine:** Implemented a standard fourth-order Runge-Kutta (RK4) integrator with adaptive time-stepping to preserve trajectory integrity across high-gradient vector fields.
* **Bifurcation Analysis:** Mapped phase-space trajectories across a spectrum of Rayleigh numbers ($\rho$). Safely isolated the subcritical Hopf bifurcation ($\rho \approx 24.74$) where steady-state fixed points lose stability, giving rise to the iconic "butterfly" strange attractor.
* **Chaos Quantification:** Evaluated sensitive dependence on initial conditions (SDIC) by tracking twin trajectories with an initial perturbation of $\delta \sim 10^{-8}$, calculating the maximal Lyapunov exponent ($\lambda_{max} > 0$) to verify true deterministic chaos rather than numerical noise.
* **Topology Mapping:** Visualized 3D phase-space projections, plotting the dual-wing geometry to study trajectory ergodicity and fractal structure bounds.

### [Lagrangian Mechanics: The Double Pendulum](https://github.com/rcgiri-physics/double-pendulum-simulation)
An examination of multi-degree-of-freedom systems and the explicit onset of deterministic chaos through analytical mechanics.

* **Euler-Lagrange Derivation:** Formulated the coupled, highly non-linear transcendental equations of motion using generalized coordinates ($\theta_1, \theta_2$).
* **Phase-Space Mapping:** Isolated the transition boundaries where regular, low-energy invariant tori break apart into high-energy chaotic seas.
* **Poincaré Sections:** Generated state-space slices to visually map the breaking of system integrability and track coordinate divergence.

### [3-Body Laboratory: Symplectic Physics Engine](https://github.com/rcgiri-physics/three-body-simulation)
A high-precision study of gravitational stability, transition to chaos, and long-term orbital conservation.

* **Symplectic Engineering:** Developed a custom Velocity-Verlet (Leapfrog) engine in Python to eliminate numerical energy dissipation, maintaining a relative Hamiltonian error of $\sim 10^{-9}$.
* **Chaos Quantification:** Identified a critical velocity perturbation threshold ($\delta \approx 0.5$) for stellar ejection using Lyapunov divergence mapping.
* **Astronomical Validation:** Verified engine stability through a 12-year simulation of the Sun-Earth-Jupiter system using Astronomical Units and Solar Masses ($G = 4\pi^2$).
* **Visualization:** Authored a cinematic rendering suite to visualize "Butterfly Effect" divergence and total system collapse.

### [Driven LCR-Series Circuit Modernization](https://github.com/rcgiri-physics/LCR-Circuit-Modernization)
A structural migration of a 2023 procedural Fortran 90 dissertation into a high-performance, vectorized Python framework.

* **Numerical Validation:** Verified custom RK4 algorithms against SciPy, achieving a maximum residual error of $< 10^{-7}$.
* **Legacy Cross-Validation:** Achieved 100% trace overlap between modern Python outputs and legacy Fortran data.
* **Performance Auditing:** Benchmarked Python interpreter loops versus compiled Fortran for 1,000,000-step execution cycles.

### [Projectile Simulation](https://github.com/rcgiri-physics/projectile-simulation)
An investigation of ballistics kinematics evaluating the transit from idealized vacuum baselines to dissipative media.

$$
m \frac{d\mathbf{v}}{dt} = m \mathbf{g} - b\mathbf{v} - c|\mathbf{v}|\mathbf{v}
$$

*   **State-Space Vectorization:** Implements array-based evaluations in NumPy to resolve non-linear quadratic drag terms where exact analytical solutions are unavailable.
*   **Error Benchmarking:** Compares custom discrete step allocations against adaptive-step algorithms to map absolute spatial residuals.

---

## 2026 Research Roadmap

| **Month** | **Project Focus** | **Technical Milestones / Status** |
| :--- | :--- | :--- |
| **Jan** | Projectile v1.0 | **Completed** • Kinematics, Euler integration, pure Python baseline. |
| **Feb** | Projectile v2.1 | **Completed** • RK4 Engine development, NumPy vectorization, SciPy validation. |
| **Apr** | LCR_Modernization | **Completed** • Fortran-to-Python pipeline, profiling, state-space phase mapping. |
| **Apr** | Chaotic 3-Body Dynamics | **Completed** • Symplectic Velocity-Verlet, Hamiltonian conservation tracking, ejection thresholds. |
| **May** | Lagrangian Mechanics | **Completed** • Double Pendulum derivation, generalized coordinates, Poincaré sections. |
| **May** | Lorenz Attractor | **Completed** • Bifurcation mapping, Chaos quantification ($\lambda_{max}$), 3D phase topology. |
| **June** | **Computational Linear Algebra** | **Next Up** • Matrix Mechanics, Eigenvalue problems, Lanczos algorithm, and Normal Mode analysis. |

---

## Computational Methodologies

My technical stack maps directly to strict methodological requirements designed for reproducible execution on standard consumer hardware (16 GB RAM, CPU-only):

* **Numerical Integration:** Symplectic algorithms (Leapfrog/Verlet) and adaptive high-order solvers (RK45, DOP853).
* **State-Space Modeling:** Vectorized array operations using NumPy and SciPy for multi-variable ODEs.
* **Chaotic Quantification:** Implementation of phase-space metrics, including Lyapunov exponents and Poincaré mapping.
* **Physics Validation:** Test-driven workflows designed to verify structural invariants (e.g., energy and momentum conservation) during runtime.
* **Environment Reproducibility:** Strict adherence to deterministic random seed controls and continuous versioning for repository continuity.

## The Research Trajectory

**Consolidated Knowledge**
I have verified my capacity to construct vectorized ODE solvers for many-body and chaotic systems. I can successfully track structural conservation laws directly within computation loops, quantify non-linear trajectories using established chaos indicators, and enforce mathematical accuracy over millions of integration steps.

**Targeted PhD-Level Methodologies (Future Research Roadmap)**
To transition from standalone numerical simulations to high-performance, doctoral-level research, I have identified the following computational methodologies as the core technical objectives of my upcoming academic trajectory:

1. **Compiled Acceleration:** Migrating computationally intensive components from interpreted Python to compiled frameworks (Numba, native C++ extensions) to bypass interpreter overhead and execute high-speed multi-parameter sweeps.
2. **Dimensional Scaling:** Progressing from systems governed by Ordinary Differential Equations (ODEs) to high-dimensional Partial Differential Equations (PDEs) and large many-body lattice matrices.
3. **Parallelization:** Implementing multi-core CPU parallelization architectures to manage large-scale computational execution and high-density state-space mapping efficiently.

---

> "Physics is the only profession in which prophecy is not only allowed but required." — This profile tracks my progress in mastering those prophecies through code.
