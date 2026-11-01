# Experiment Log

## Experiment 001 — Cantilever beam: baseline FEM simulation

**Objective:** Simulate the bending of a cantilever beam and compare the FEM results with Euler–Bernoulli beam theory.

### Model setup

| Parameter | Value |
|---|---:|
| Length | 200 mm |
| Width | 20 mm |
| Height | 10 mm |
| Material | Steel |
| Young's modulus | 210 GPa |
| Applied load | 10 N initially; subsequently tested at 20 N |
| Support | One end fixed |
| Solver | CalculiX 2.23 |
| Mesher | Netgen |

### Analytical calculations

Second moment of area:

I = bh³/12 = 1666.7 mm⁴

For an end-loaded cantilever:

δ = PL³/(3EI)

At 10 N, theoretical tip deflection is approximately 0.0762 mm.

At 20 N, theoretical tip deflection is approximately 0.1524 mm.

Maximum bending stress:

σ = 6PL/(bh²)

At 20 N, theoretical maximum bending stress is approximately 12 MPa.

### Observations

- Doubling the load approximately doubled the displacement, consistent with linear elastic behaviour.
- Mesh refinement changed the displacement result significantly.
- With a refined mesh, displacement was approximately 0.15 mm.
- Maximum von Mises stress was approximately 11.22 MPa.
- The refined results were reasonably close to analytical beam theory.

### Lessons

- Boundary conditions and load direction matter.
- Mesh density can significantly affect FEM results.
- Analytical solutions are useful for validating simulations.
- A visually plausible result is not necessarily an accurate result.

### Limitations / follow-up

- Perform a more systematic mesh-convergence study.
- Record precise displacement values for each mesh.
- Compare stress away from local constraint and load application effects.
- Investigate how changing beam height affects bending stiffness.

---

## Future experiments

Add new experiments below as they are completed. Give each experiment its own objective, setup, analytical reference, observations, and conclusions.
