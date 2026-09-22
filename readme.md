# Numerical Methods for Electrical Engineering (EE4001-IC)

## Section 1: Introduction

Welcome to <i>Numerical Methods for Electrical Engineering</i> (EE4001-ic)! 

In the <i>Numerical Methods for Electrical Engineering project</i>, you will be building and testing a simulation software. This software should enable the modelling of the electro-mechanical behavior of linear actuators in a transient regime. Two test cases will be available. The first is a hybrid reluctance actuator. The second is a haptic resonant actuator. The end-users of your software include PhD researchers and engineers at high precision manufacturing company. Teamwork is essential because of the complex nature of the challenge. Starting from the application scenarios and operation principles, your team will choose a specific actuator and define a program of requirements for the simulation software. Based on the program of requirements, your team will apply both mathematical skills and electrical engineering knowledge to define the physical problem. You will employ concepts of mathematical modeling. You implement numerical solving routines for both initial value problems and boundary value problems. To guide the transition in complexity, the project is divided into three blocks. By the end of the project, your team should be able to simulate how the actuator moves with given electrical excitation. You will be given intermediate feedback and write an incremental design and test report throughout the project and will be assessed based on the report.

### Section 1.1: Learning Activities 

### Section 2.1: Assessment

### Section 3.1: Electrical Engineering
1. linear actuators, hybrid reluctance actuator, haptic actuator; 
2. numerical models for linear actuators, equivalent circuit models, finite element models;

### Section 4.1: Numerical Methods 
1. partial differential equations, ordinary differential equations, boundary conditions, initial conditions, reference solution (analytical, symbolic or reference packages), finite element method (Galerkin weak form, element-by-element construction of linear system, linear system solve);

### Section 5.1: Software Implementation 
1. home-brewed finite element simulator in Julia programming language. Preprocessor for geometry and mesh. Visualization and postprocessing of the computed solution. 
2. motivate the choice for Julia: computationally efficiently while easier to use than classical programming languages

## Section 2: First Block: Physical Principles and One-Dimensional Models  

In the first block we introduce numerical methods for the design of linear actuators. 

### Section 1.2: Electrical Engineering
1. physical principles of linear actuator: magnetic laws, derive voltage equations and the flux linkage equations from Newtons Law of motion, mechanical laws, derive an expression for the magnetic force from the magnetic circuit equations.
2. introduction to systems of ordinary differential equations, both in space and in time, state space representation; 
3. analytical solution of system of first order equations 

### Section 2.2: Numerical Methods 

### Section 3.2: Software Implementation 
1. Julia programming language (how does this overlap with EE part?); 
2. 1D FEM code; 

### Section 4.2: References  

<b>Reference Software Components</b>
1. One-dimensional linear shape functions Galerkin finite element code 
2. Boundary and initial value problems using the function <i>dsolve</i> in sympy; 

<b>Reference Slides</b> 
1. [one-dimensional finite element method](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/block1-finite-element-method-1d.pdf)
2. [mathematical preliminaries slides](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/mathematical-preliminaries.pdf)
3. [modeling fields slides](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/modeling-fields.pdf)

## Section 3: Second Block: Time Integration and Two-Dimensional Models 

In the second block we describe more versatile numerical methods.

### Section 1.3: Electrical Engineering
1. various ODE numeric solvers, choices, Euler forward method, stability issue, Euler backward for linear system, own implementation, compare with DifferentialEquations.jl to benchmark the implementation;  
2. coupling to FEM model by magnetic flux through a surface, force (Lorenz and Maxwell stress tensor) and energy (by integrating the energy density); 
3. prescribed flux vs. (pos, current)
4. solve the numerical model with given inputs

### Section 2.3: Numerical Methods 

### Section 3.3: Software Implementation 

### Section 4.3: References  

<b>Reference Slides</b> 
1. [two-dimensional finite element method](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/block2-finite-element-method-applications.pdf) 
   
## Section 4: Third Block: Linear Actuator Application 

In the third block we apply numerical methods to the design of linear actuators. 

### Section 1.4: Electrical Engineering
1. coupling to 2D FEM: use FEM to compute flux for various current values; Alternatively, provide a precomputed current-flux curve; 
2. discretization of ODE model (same as block-1) by first order hold method  for digital control: first by hand - later validated with ControlSystems.jl;. 
3. valuate the linear dynamics of ODE models by eigenvalues and eigenvector analysis with numerical tools - Bode plot in frequency domain - interpretation of the results obtained

### Section 2.4: Numerical Methods 

### Section 3.4: Software Implementation 

### Section 4.4: References  

## Section 5: Linear Actuator Models 

### Section 1.5: Hybrid Reluctance Actuator 

<b>Pre-processing</b>:  
1. script to generate geometry model using OpenCascade. Document subdomain labels for core, mover, coils, magnet and air subdomain; 
2. script to generate mesh using GMSH. Indicate further work required to refine the mesh in the airgap;
3. sample mesh file; 

<b>Computational Kernel</b>: Using linear triangular elements implemented in a home-brewed implementation. Still requires force computation using the virtual energy principle; 

<b>Post-processing</b>: VTK file with simulation results;  

### Section 2.5: Haptic Actuator 

<b>Pre-processing</b>: Geometry model, mesh generation and sample mesh file; 

<b>Computational Kernel</b>: Finite element simulation; 

<b>Post-processing</b>: VTK file with simulation results;  

## Section 6: Course Design Document 

## Section 7: References

### References on Software Components for Pre-Processing 
1. [GMSH](https://gmsh.info)
2. [OpenCascade](https://occt3d.com/open-cascade-technology/index.html)

### References on Software Components for Computational Kernel 
1. [Julia programming language](https://julialang.org)
2. [Ferrite FEM package](https://ferrite-fem.github.io/Ferrite.jl/stable/)
3. [Scientific machine learning](https://sciml.ai)

### References on Software Components for Post-Processing
1. [WriteVTK.jl](https://github.com/JuliaVTK/WriteVTK.jl)
2. [Paraview](https://www.paraview.org)

### References on the Finite Element Method 

1. [Introduction to Numerical Methods for Variational Problems](https://link.springer.com/book/10.1007/978-3-030-23788-2) by Hans Petter Langtangen and Kent-Andre Mardal. The [book](https://link.springer.com/book/10.1007/978-3-030-23788-2) is freely available; 
2. [Wolfgang Bangerth's video lectures](https://www.math.colostate.edu/~bangerth/videos.html); 
3. [wiki Finite Element Method](https://en.wikipedia.org/wiki/Finite_element_method): Section 3 for the weak form and Section 4 for the finite element discretization;  
4. [Comsol Multiphysics Finite Element Method](https://www.comsol.com/multiphysics/finite-element-method): more information and illustrations; 
5. [Comsol Multiphysics Brief Introduction to the Weak Form](https://www.comsol.com/blogs/brief-introduction-weak-form): good introduction to a theoretical concept that provides a basis for the finite element method; 
6. [Ferrite Introduction to FEM](https://ferrite-fem.github.io/Ferrite.jl/stable/manual/fe_intro/)
7. [Sphinx Finite Element Method](http://hplgit.github.io/INF5620/doc/pub/sphinx-fem/): reference for implementation;


```julia

```
