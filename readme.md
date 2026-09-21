# Numerical Methods for Electrical Engineering (EE4001-IC)

## Section 1: Introduction

Welcome to <i>Numerical Methods for Electrical Engineering</i> (EE4001-ic)! 

In the <i>Numerical Methods for Electrical Engineering project</i>, you will be building and testing a simulation software. This software should enable the modelling of the electro-mechanical behavior of linear actuators in a transient regime. Two test cases will be available. The first is a hybrid reluctance actuator. The second is a haptic resonant actuator. The end-users of your software include PhD researchers and engineers at high precision manufacturing company. Teamwork is essential because of the complex nature of the challenge. Starting from the application scenarios and operation principles, your team will choose a specific actuator and define a program of requirements for the simulation software. Based on the program of requirements, your team will apply both mathematical skills and electrical engineering knowledge to define the physical problem. You will employ concepts of mathematical modeling. You implement numerical solving routines for both initial value problems and boundary value problems. To guide the transition in complexity, the project is divided into three blocks. By the end of the project, your team should be able to simulate how the actuator moves with given electrical excitation. You will be given intermediate feedback and write an incremental design and test report throughout the project and will be assessed based on the report.

### Section 1.1: Learning Activities 

###  Section 2.1: Assessment 

## Section 2: First Block: Physical Principles and One-Dimensional Models  

### Section 1.2: Reference Slides 
1. [one dimensional finite element method](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/block1-finite-element-method-1d.pdf)
2. [mathematical preliminaries slides](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/mathematical-preliminaries.pdf)
3. [modeling fields slides](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/modeling-fields.pdf)

## Section 3: Second Block: Time Integration and Two-Dimensional Models 

### Section 1.3: Reference Slides 
1. [two dimensional finite element method](https://github.com/ziolai/finite_element_interdisciplinary_challenge/blob/main/slides/block2-finite-element-method-applications.pdf) 
   
## Section 4: Third Block: Linear Actuator Application 

In the third and last block we discuss the finite element solution of the Poisson equation in two spatial dimension. We discuss the mesh generation using triangle and the construction of the discrete problem using a loop over all elements. We illustrate the method in the computation of magnetostatic fields in transformers and electrical machines.  
## Section 5: Linear Actuator Models 

### Section 1.5: Hybrid Reluctance Actuator 

<b>Pre-processing</b>: Geometry model, mesh generation and sample mesh file; 

<b>Computational Kernel</b>: Finite element simulation; 

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
