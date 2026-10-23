# Ram Chandra Giri

**MSc Physics · Physics educator · Preparing for a PhD in Computational Physics & Nonlinear Dynamics** · Nepal
[ORCID 0009-0008-7149-7938](https://orcid.org/0009-0008-7149-7938)

I model non-linear and chaotic systems with my own integrators, and I check every result against a conservation law or an independent reference. Each repository is written up like a lab entry: the system, the method, and the check used to trust it.

**Research interests:** Hamiltonian and dissipative chaos, symplectic integration, verification of scientific software.

| Status · Oct 2026 | |
| :--- | :--- |
| Physics projects | 5 completed (MSc dissertation: driven LCR circuits, Fortran 90, 2023) |
| Research software | [physverify](https://github.com/rcgiri-physics/physverify) v0.4.2 (PyPI, DOI) |
| Applied work | [MCQplex](https://mcqplex.com) (live) |
| Next | Computational linear algebra, from Nov 2026 |
| Hardware | 16 GB RAM, CPU-only, by design |

---

## Main work: physverify

**[physverify](https://github.com/rcgiri-physics/physverify)** checks that a simulation solves the equations it claims, at the order of accuracy it claims, not just that it runs.
[PyPI](https://pypi.org/project/physverify/) · [Docs](https://rcgiri-physics.github.io/physverify/) · [doi:10.5281/zenodo.23534512](https://doi.org/10.5281/zenodo.23534512) · GitHub Action

- Convergence-order, conservation and manufactured-solution checks for ODE and 1D PDE solvers; static `scan` of Runge-Kutta tables, grid spacings and physical constants. Needs only NumPy.
- Flagged 35 of 37 seeded bugs, with no false alarms (bugs and checks written by the same person, so this shows it works as designed).
- Applied to public physics repositories: 74 defects reported to their authors ([which method found each](https://github.com/rcgiri-physics/physverify/blob/main/results/corpus/FINDINGS_BY_METHOD.md)).
- Limits are stated plainly: works best for ODEs, and a PASS means "these checks found nothing", not "proven correct".

## Experiments

| Project | Method | Check used to trust it |
| :--- | :--- | :--- |
| [3-Body Laboratory](https://github.com/rcgiri-physics/three-body-simulation) | Symplectic Velocity-Verlet; Sun-Earth-Jupiter over 12 years | Relative energy error ~10⁻⁹; ejection threshold δ ≈ 0.5 |
| [Lorenz Attractor](https://github.com/rcgiri-physics/lorenz-attractor-simulation) | Adaptive RK4; bifurcation sweep over ρ | λ_max > 0 from twin trajectories at δ ~ 10⁻⁸ |
| [Double Pendulum](https://github.com/rcgiri-physics/double-pendulum-simulation) | Euler-Lagrange in (θ₁, θ₂) | Poincaré sections: invariant tori breaking into chaos |
| [Driven LCR Circuit](https://github.com/rcgiri-physics/LCR-Circuit-Modernization) | 2023 Fortran 90 dissertation rebuilt in vectorised Python | Residual vs SciPy < 10⁻⁷; matches legacy Fortran output |
| [Projectile Simulation](https://github.com/rcgiri-physics/projectile-simulation) | Vacuum to linear + quadratic drag; fixed vs adaptive steps | Spatial residual maps |

## 2026 log

| Month | Work | Status |
| :--- | :--- | :--- |
| Jan–Feb | Projectile v1.0 → v2.1: Euler, then RK4 validated against SciPy | Done |
| Apr | LCR modernisation; chaotic 3-body dynamics | Done |
| May | Double pendulum; Lorenz attractor | Done |
| Jun–Sep | [MCQplex](https://mcqplex.com) (NEB exam prep), school routine planner, [llm-free-cascade](https://github.com/rcgiri-physics/llm-free-cascade), [pdf-render-pool](https://github.com/rcgiri-physics/pdf-render-pool), [mongo-job-lock](https://github.com/rcgiri-physics/mongo-job-lock) | Live / released |
| Oct | [physverify](https://github.com/rcgiri-physics/physverify) 0.1 → 0.4.2: verification tool for simulations | Released |
| **Nov →** | **Computational linear algebra:** eigenvalue problems, Lanczos, normal modes | **Next** |

**Toward PhD-level work:** compiled acceleration (Numba, C++) → PDEs and lattice systems → multi-core parameter sweeps.

## Applied work and open source

- **[MCQplex](https://mcqplex.com)**: adaptive NEB exam prep for low-end Android and patchy networks, with teacher analytics and practice duels.
- **Routine & Substitution Planner**: offline-first school timetable with a tiered teacher-substitution engine.
- **Open curricula** (v0.1, not yet piloted in a classroom): [git-for-schools](https://rcgiri-physics.github.io/git-for-schools/) (offline-first Git, Grades 8–12) · [data-science-nepal](https://rcgiri-physics.github.io/data-science-nepal/) (bilingual, Nepali datasets).
- **Utilities**: [llm-free-cascade](https://github.com/rcgiri-physics/llm-free-cascade) (free-tier LLM fallback) · [pdf-render-pool](https://github.com/rcgiri-physics/pdf-render-pool) (Puppeteer HTML→PDF pool) · [mongo-job-lock](https://github.com/rcgiri-physics/mongo-job-lock) (run a clustered cron job once).

---

> "Physics is the only profession in which prophecy is not only allowed but required."
