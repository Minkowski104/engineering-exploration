# Learning roadmap

## Guiding approach
Explore through practical engineering questions. Build enough theory to interpret results, but avoid turning the process into an extended textbook-only exercise or committing too early to one specialization.

## Current sequence

### 1. Structural mechanics and FEM
Current focus: cantilever beam in FreeCAD FEM / CalculiX.

Suggested next experiments:
- Change beam height and compare deflection with the \(h^3\) dependence of second moment of area.
- Double the load and check linear scaling under linear-elastic assumptions.
- Compare multiple mesh sizes and record precise outputs for a mesh-convergence study.
- Optionally compare a tapered beam with a uniform beam.

Move on once the basic workflow and validation are understood; do not aim to exhaust FEM theory first.

### 2. Fluid mechanics and CFD
Next broad area: OpenFOAM and ParaView.

A motivating class of problems is liquid flow, such as a hot fluid stream pouring into a receiving vessel, with interest in flow structure and temperature distribution. Begin with a simpler canonical case before attempting a complex free-surface, heat-transfer simulation.

### 3. CAD and automation
Continue parametric modelling in FreeCAD. Explore scripting and automation where they help connect geometry, simulation, and software.

### 4. Thermal systems and robotics
Explore heat transfer, control systems, dynamics, and robotics as interests develop.

## Planning constraint
Keep the workload sustainable alongside professional work. A rough target discussed previously was a few hours per week, not a strict commitment.
