# PDE-Solver
This project implements a **numerical solver for the incompressible Navier–Stokes equations** coupled with the **heat (advection–diffusion) equation**, enabling realistic simulation of fluid flow with thermal transport, using the pytorch library.

$$\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{u} = -\nabla p + \nu \nabla^2 \mathbf{u} + \mathbf{f}(T) $$

$$ \frac{\partial T}{\partial t} + \mathbf{u} \cdot \nabla T = \alpha \nabla^2 T $$

The solver iteratively applies the given differential equations while maintaining the **incompressibility constraint** $\nabla \cdot \mathbf{u} = 0 $.

- **Time integration:** Semi-implicit scheme with explicit advection  
- **Pressure solve:** Poisson equation solved via iterative methods  
- **Advection:** Upwind / semi-Lagrangian hybrid  
- **Diffusion:** Central finite differences  
- **Boundary conditions:** No-slip walls, inflow/outflow, and thermal Dirichlet or Neumann conditions  

![Image](projects/pde-solver.gif)

More information about the implementation can be found on the [github page](https://github.com/jakobscharf "PDE-Solver for Navier-Stokes/Heat").
