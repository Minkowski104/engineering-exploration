# FreeCAD FEM — cantilever beam

## Environment
- FreeCAD on Intel Mac, macOS 14.8.
- CalculiX executable: `/Applications/FreeCAD.app/Contents/Resources/bin/ccx`
- CalculiX version observed: 2.23.
- Netgen mesher.

## Model geometry
Rectangular cantilever beam:
- Length \(L = 200\,\mathrm{mm}\)
- Width \(b = 20\,\mathrm{mm}\)
- Height \(h = 10\,\mathrm{mm}\)
- Steel, Young's modulus \(E = 210\,\mathrm{GPa} = 210000\,\mathrm{N/mm^2}\)
- One end fixed; force applied at the opposite end face.

The model file was copied into:
`structural-mechanics/cantilever-beam/models/Cantilever_beam.FCStd`

## Analytical reference
Second moment of area for bending about the relevant axis:
\[
I = \frac{bh^3}{12} = \frac{20(10)^3}{12} = 1666.7\,\mathrm{mm^4}
\]

For an ideal end-loaded cantilever:
\[
\delta = \frac{PL^3}{3EI}
\]

At \(P=10\,\mathrm{N}\), \(\delta \approx 0.0762\,\mathrm{mm}\).

At \(P=20\,\mathrm{N}\), \(\delta \approx 0.1524\,\mathrm{mm}\).

Maximum bending stress at the fixed end:
\[
\sigma_{max} = \frac{Mc}{I} = \frac{6PL}{bh^2}
\]

At \(P=20\,\mathrm{N}\), \(\sigma_{max} \approx 12\,\mathrm{MPa}\).

## Observations recorded
- Doubling the load from 10 N to 20 N approximately doubled displacement, consistent with linear-elastic behaviour.
- With a coarse mesh (maximum element size around 5 mm), the reported displacement at 10 N was around 30.43 µm in one result.
- Refining the mesh changed the result substantially.
- With a refined mesh (maximum element size around 2 mm, then around 1 mm), the reported displacement magnitude was approximately 0.14–0.15 mm for the 20 N case.
- A reported maximum von Mises stress was 11.22 MPa.
- The refined displacement and stress are encouragingly close to beam-theory estimates, but displayed displacement values were rounded and a systematic convergence study has not been completed.

## Important caveats
- Do not claim a precise percentage error from the rounded 0.15 mm result.
- Record the exact load and mesh settings for each future run; do not assume all screenshots/results correspond to the same setup.
- Compare stress away from local load/support effects where appropriate.
- A warning appeared about a material object's reference shape being ignored. Its significance was not established; do not present it as the cause of discrepancies without evidence.
- A reaction-force output for the 10 N run showed approximately +10 N in the vertical direction, with near-zero other components, consistent with force equilibrium.

## Next experiments
1. Change beam height (for example, from 10 mm to 15 mm) and compare deflection with the \(h^3\) stiffness dependence.
2. Check load scaling with a controlled pair of runs.
3. Perform a mesh-convergence study, recording exact displacement and stress values for each mesh.
