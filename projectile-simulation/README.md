# Projectile motion: From Vacuum to Quadratic Drag

A computational physics study comparing analytical and numerical solution for motion in a fluid.

## Introduction

This project simulates the trajectory of a projectile under three different physical models. It demonstrates the transition from simple classroom physics to realistic, non-linear systems that require numerical integration.

**Note:** *Version 1.0* implements a manual time-stepping algorithm (Euler Method) using standard Python data structures (lists) to avoid dependency on heavy numerical libraries. it is worth noting that the Euler method is a "first-order" numerical method. This means its global error is roughly proportional to the time step $\Delta t$. It is only accurate for very small time steps, so, later version we will move to *SciPy* and *RK4*.

## 1. Physical models

For all three cases, we start with Newton's Second Law:

$$\sum\vec{F}=m\vec{a} => m\frac{d\vec{v}}{dt}=m\vec{g}+\vec{F}_{drag}$$

To solve this numerically in Python, we split the second-order equation into two first-order equations for each dimension (x and y)

$$\frac{dx}{dt}=v_x, \frac{dy}{dt}=v_y$$

### Case A: Ideal motion (Vacuum)

In a vacuum, the only force is gravity

- Equation of motion

$$\frac{d\vec{v_x}}{dt} = 0,  \frac{d\vec{v_y}}{dt} = -\vec{g}$$

- Analytical Solution:

$$x(t) = v_{0x}t$$

$$y(t) = v_{0y}t - \frac{1}{2} gt^2$$

- Solving parameters: $g=9.81m/s^2$

- Physical Insight: The trajectory is a perfect parabola. The horizontal velocity $v_x$ remains constant throughout the flight.

### Case B: Linear Drag (Stokes' Drag)

Applicable for low-speed motion where $F_{drag} = -b\vec{v}$.

- Equation of motion

$$\frac{dv_x}{dt} = -kv_x, \quad \frac{dv_y}{dt} = -g - kv_y$$

- Analytical solution:

$$x(t) = \frac{v_{x0}}{k}(1 - e^{-kt})$$

- Solving Parameters:
$m$: Mass of the object.
$b = 6 \pi \eta r$ (where $\eta$ is the dynamic viscosity of the fluid).

- Physical Insight: The equations are uncoupled (the $x$-motion does not affect the $y$-motion). The object approaches a terminal velocity $v_t = \frac{mg}{b}$. It explains why we use different models. It notes that Linear Drag applies to tiny objects [cite](https://pubs.aip.org/aapt/ajp/article-abstract/67/6/538/1055298/On-the-rise-and-fall-of-a-ball-with-linear-or) (like dust or oil droplets, $Re < 1$) while Quadratic Drag applies to sports balls ($Re > 1000$). Fixed coefficients are used in the simulation for clarity only.

### Case C: Quadratic drag (Newtonian Drag)

The most realistic model for macroscopic objects where $\vec{F}_{drag} = -cv\vec{v}$.
$\vec{F}_{drag} = -\frac{1}{2} C_d \rho A |\vec{v}| \vec{v}$

- Differential Equations:
$$\frac{dv_x}{dt} = -\frac{1}{m} \left( \frac{1}{2} C_d \rho A \sqrt{v_x^2 + v_y^2} \right) v_x$$$$\frac{dv_y}{dt} = -g - \frac{1}{m} \left( \frac{1}{2} C_d \rho A \sqrt{v_x^2 + v_y^2} \right) v_y$$

- Solving Parameters:
$\rho$: Density of air ($\approx 1.225 \, \text{kg/m}^3$ at sea level).
$C_d$: Drag coefficient ($0.47$ for a sphere).
$A$: Cross-sectional area ($\pi r^2$).

- Physical Insight: The equations are coupled because the total speed $|\vec{v}|$ affects both components. The object approaches a terminal velocity $v_t = \sqrt{\frac{2mg}{\rho C_d A}}$. There is no simple analytical solution; numerical integration (like RK4) is mandatory.

## 2. Numerical Implementation

In classical mechanics, we describe motion using continuous differential equations:$$\frac{d\vec{v}}{dt} = \vec{a}$$

To solve this in Python, we discretize time into small steps $\Delta t$. We approximate the change in velocity and position as:$$v_{n+1} = v_n + a_n \Delta t$$$$s_{n+1} = s_n + v_{n+1} \Delta t$$

Also, since the quadratic case has no closed-form analytical solution, we necessarily need to use numerical (version 1.0) methods to solve this problem.

## Validation

To ensure the solver's accuracy, I compared the **Vacuum and Linear Drag** numerical output against the exact exponential analytical solution. The error was minimized to 10⁻⁶, confirming the code's reliability.

## 3. Results and Visualization

The simulation generates three key insights:

- Reliability (Validation)

We validated the Euler solver against the exact analytical solution for Linear Drag. As shown below, the numerical error is negligible for our time step.
![Validation Plot](plots/1_validation_error.png)

- Physical Models Comparison

Comparing the three drag models shows that quadratic drag (realistic air resistance) significantly reduces range compared to the vacuum ideal.
![Comparison Plot](plots/2_model_comparison.png)

- Effect of Mass

Unlike in a vacuum, mass matters in air. Heavier objects (blue/green) maintain momentum better and travel further than lighter objects (red/orange) which are easily slowed by air resistance.
![Mass Plot](plots/3_mass_variation.png)

## 4. How to Run

1. Ensure you have Python installed.
2. Install dependencies: `pip install matplotlib`
3. Run the script: `python projectile_sim_v1.py`

## 5. Future Enhancements

1. Update Euler's method to Runge-Kutta 4th Order (RK4) or Python libraries that solve ODEs like `scipy.integrate.solve_ivp` {Version 2.0}
2. Incorporate the Magnus Effect (spin on the ball)
3. Add a Variable Density Atmosphere model for high-altitude projectiles
4. Implement a GUI using TKinter or PyQt for real-time parameter adjustment

## 6. References & Resources

- For the Core Physics: Taylor, J.R. (2005). *Classical Mechanics.* University Science Books. (Chapter 2 covers Projectiles and Air Resistance.)
- For Fluid Dynamics (Drag): [NASA Glenn Research Center. The Drag Equation.](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/drag-of-a-sphere/)
- For Numerical Methods: Press, W.H., et al. *Numerical Recipes: The Art of Scientific Computing.* Cambridge University Press

## 7. Conclusion: Insight from the simulation

The primary objective of this project was to transition from the idealized "vacuum" model of projectile motion to a realistic simulation incorporating fluid dynamics. Several key physical insights were discovered through the numerical results:

1. The Breakdown of Symmetry
In a vacuum, the trajectory is a perfectly symmetric parabola. However, once air resistance (Linear or Quadratic) is introduced, this symmetry is broken. The "descent" phase is always steeper than the "ascent" phase because the drag force continuously drains the kinetic energy of the system, leading to a shorter range and a lower peak height.
2. Optimal Launch Angle
While the theoretical maximum range in a vacuum is achieved at 45 degrees, this simulation demonstrates that in a medium with quadratic drag, the optimal angle shifts downward. For a standard projectile (like a ball), the maximum range is typically found between 35 and 40 degrees. This is because a lower angle reduces the "Time of Flight", thereby reducing the total time the drag force has to act on the horizontal velocity.
3. Numerical Reliability
By comparing the numerical results of the Linear Drag model with its Analytical Solution, the error was found to be in the order of 10⁻⁶ or less.
4. Mass Variation
Heavier objects have more inertia relative to their surface area, making them less affected by air resistance than lighter objects.
5. Final Reflection
This project demonstrates the necessity of computational methods in Physics. While simple models can be solved with pen and paper, "real-world" physics—where the forces are coupled and non-linear—requires the power of numerical integration.

This simulation serves as a foundational step toward more complex models involving the Magnus Effect (lift from spin) or Variable Air Density.
