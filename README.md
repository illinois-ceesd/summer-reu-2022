# CEESD Summer REU Tutorials

These tutorials are designed to acquaint undergraduate computer science and engineering students with the physical and computational principles underlying [MIRGE-Com](https://github.com/illinois-ceesd/mirgecom), a software library developed by the [Center for Exascale-Enabled Scramjet Design](https://ceesd.illinois.edu/) for simulating scramjets on distributed systems.


## Agenda

0. [The Physics of Scramjets](./0-physics.md) · 6/14 (Mon)
1. [Discretization & Mapping](./1-discrete.md) · 6/25 (Fri)
2. [Grid Data Structures](./2-griddata.md) · 7/2 (Fri)
3. [Transport on Grids](./3-transport.md) · 7/12 (Mon)
4. [Matrix Solvers & Conditioning](./4-solvers.md) · 7/16 (Fri)
5. [Shock Modeling](./5-shocks.md) · 7/23 (Fri)
6. [Software Quality/V&V](./6-verval.md) · 7/30 (Fri)
7. [Chemistry Modeling in Flows](./7-chemrxn.md) · 8/2 (Mon)


## Expected Background

- **Python**.  MIRGE-Com is written in Python; although the lessons make oblique explanatory references to other languages like C, only familiarity with Python is expected to complete these lessons and contribute to MIRGE-Com.
- **Physics**.  The lessons do not assume any particular background in physics or engineering other than a freshman-physics understanding of heat transfer, conservation laws, etc.; other properties are derived.  Naturally, the student will glean greater insight given a more advanced background.
- **Mathematics**.  The student will need calculus (at least Cal 1, but Cal 3 preferred) and some basic linear algebra.  Numerical analysis is helpful as well.


## Preparation

Review [“MIRGE-Com Development How-To”](https://mirgecom.readthedocs.io/en/latest/development/development.html).  If you will run MIRGE-Com on your own system, install it locally.

You may also find it convenient to install [Paraview](https://www.paraview.org/download/) locally for visualizing results.  (Load the `pvtu` file to view all output in a time series.)


## Operation

The Python virtual environment for MIRGE-Com may be activated in a single line in each terminal session before running code:

```sh
. miniforge3/bin/activate ceesd
```

---

The lessons cover most of the following points at least glancingly, except for discrete simulation methods, wall functions, coupling, turbulence modeling, time-resolved (transient) flow, and particulars of HPC execution.

-   Physics
    -   Problem Statement
    -   Governing Equations
    -   Physical Models
        -   Turbulence (DNS, Large Eddy Simulation, k-Epsilon, etc.)
    -   Assumptions & Simplifications
-   Grid
    -   Geometry
    -   Structure
    -   Special Requirements
        -   Wall functions
        -   Coupling
-   Discretization
    -   Discretization Method
    -   Accuracy
    -   Implicit v. Explicit Formulations
    -   Elements
-   Solution
    -   Algorithms
        -   Traditional Methods:
            -   Finite Difference Method (FDM)
            -   Finite Element Method (FEM)
            -   Finite Volume Method (FVM)
        -   Discrete Simulation or Particle methods
            -   lattice gas automata (LGA)
            -   lattice Boltzmann equation (LBE)
            -   discrete velocity methods (DVM)
            -   dissipative particle dynamics (DPD)
            -   smoothed-particle hydrodynamics (SPH)
            -   direct simulation Monte Carlo (DSMC)
            -   stochastic rotation dynamics (SRD)
            -   molecular dynamics (MD)
            -   hybrid methods
    -   Steady-State v. Transient Flow
    -   Simulation Execution
        -   HPC capability computing (maximum compute power to solve a single large problem in the shortest amount of time)
        -   HPC capacity computing (most efficient configuration to solve multiple complex problems simultaneously)
    -   Convergence
-   Analysis
    -   Verification & Validation
    -   Postprocessing & Visualization
    -   Interpretation of Results

---

These tutorials were prepared by N E Davis for the [Center for Exascale-Enabled Scramjet Design](https://ceesd.illinois.edu/) in 2021.  The program's design was inspired by the [Los Alamos National Laboratory Computational Physics Student Summer Workshop](https://www.lanl.gov/org/padwp/adx/computational-physics/summer-workshop/index.php).  Some material draws from the 2015–16 course ME 498CF “Computational Fluid Dynamics”.

All materials are produced under the aegis of the University of Illinois, ©2021.  I (N E Davis) furthermore make the materials available under a [CC-BY](https://creativecommons.org/licenses/by/4.0/) license.

![](http://i.creativecommons.org/l/by/4.0/88x31.png)
