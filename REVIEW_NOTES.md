# Review before publishing numerical claims

The notebook is preserved as a record of a 2025 computational assignment; results have not been independently re-executed in this packaging step.

1. **Retrograde sign (important).** In `Omega_circular_kerr`, both returned frequencies are positive. For positive central spin and the conventions used in the README, a **retrograde orbit requires negative angular velocity**: $Ω_-=-√M/(r^{3/2}-a√M)$ in geometrized units. Update the initial conditions, re-integrate and replace related plots and the original explanation that attributes open orbits to frame dragging alone.
2. **Boyer–Lindquist visualization.** The notebook uses `x=r sinθ cosφ` etc. as an intuitive plotting map. Boyer–Lindquist coordinates are not ordinary spherical coordinates; a commonly used Kerr–Schild-type oblate projection contains factors $√(r²+a_{len}²)$ (and an azimuth convention). Label such plots as illustrative unless a verified mapping is implemented.
3. **Horizons are not singularities.** The roots $r_±=M±√(M²-a_{len}²)$ are horizon locations in geometrized coordinates; do not call them curvature singularities.
4. **Regimes of approximation.** Clearly separate the linearized Kerr metric from the full Kerr metric, and use small spin parameters consistently in first-order comparisons.
5. **Validation tests.** Check four-velocity normalization and, ideally, conserved Killing energy and angular momentum; compare against analytic circular frequencies and expected limits, with a reliable integration tolerance.
6. **Reproducibility.** `einsteinpy` symbolic computations can be slow and version-sensitive; install in a fresh environment and re-execute the entire notebook before making public numerical claims.
7. **Attribution.** The original notebook discloses assistance from ChatGPT/Gemini in selected visualization and tensor-processing cells. Preserve these acknowledgments. Check permission to make coursework public.
