# Project Status

Last updated: 2026-11-01

## Overall goal

Explore engineering disciplines through practical projects, combining mechanical engineering fundamentals with software, CAD, and simulation.

The goal is to build genuine understanding and practical skills without committing prematurely to one specialization.

## Current setup

- **Computer:** Intel Mac, 16 GB RAM, macOS Sonoma 14.8
- **CAD:** FreeCAD
- **FEM solver:** CalculiX 2.23 (bundled with FreeCAD)
- **Mesher:** Netgen
- **CFD:** OpenFOAM is a future focus

## Current project: Cantilever beam

### Model

- Geometry: rectangular beam
- Length: 200 mm
- Width: 20 mm
- Height: 10 mm
- Material: steel
- Young's modulus: 210 GPa
- Boundary conditions: one end fixed, load applied at the other end

### Completed

- Created the beam in FreeCAD.
- Set up a FEM analysis.
- Assigned material properties.
- Generated meshes using Netgen.
- Applied fixed and force constraints.
- Solved using CalculiX.
- Visualized displacement and von Mises stress.
- Refined the mesh and compared results.
- Compared simulation results against analytical cantilever beam equations.

### Analytical reference

For an end-loaded cantilever:

- Second moment of area: I = bh³/12 = 1666.7 mm⁴
- Tip deflection: δ = PL³/(3EI)
- Maximum bending stress: σ = 6PL/(bh²)

For a 20 N load:

- Theoretical tip deflection: approximately 0.1524 mm
- Theoretical maximum bending stress: approximately 12 MPa

The refined simulation gave approximately 0.15 mm displacement and 11.22 MPa maximum von Mises stress.

These are encouraging results, but a formal mesh-convergence study has not yet been completed.

## Next steps

1. Complete a few controlled FEM experiments:
   - Change beam height and compare deflection.
   - Double the applied load and check linear scaling.
   - Compare results across mesh sizes.
2. Document the experiments.
3. Move on to introductory CFD with OpenFOAM.

## Learning philosophy

Prioritize understanding physical behaviour, assumptions, boundary conditions, and numerical results over simply learning software interfaces.
