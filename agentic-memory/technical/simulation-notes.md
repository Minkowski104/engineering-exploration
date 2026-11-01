# General simulation notes

## Validation mindset
- Check units and dimensional consistency.
- Verify boundary conditions and load directions.
- Check global equilibrium where applicable.
- Compare with analytical solutions or limiting cases.
- Refine the mesh and record whether quantities of interest converge.
- Distinguish local peaks near supports, loads, sharp corners, and geometric singularities from representative field values.
- Preserve solver settings and exact output values.

## Recording an experiment
For each simulation, record:
1. Question / hypothesis.
2. Geometry and dimensions.
3. Material properties and units.
4. Boundary conditions and loads.
5. Mesh type, element order, and mesh sizing.
6. Solver and relevant settings.
7. Quantitative results.
8. Analytical or experimental comparison.
9. Interpretation, limitations, and next test.

## Evidence labels
Use explicit language:
- **Calculated:** derived from an equation or script.
- **Simulated:** returned by a solver.
- **Observed:** seen in a plot or interface.
- **Assumed:** selected but not independently verified.
