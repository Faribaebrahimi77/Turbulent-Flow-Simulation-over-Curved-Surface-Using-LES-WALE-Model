# Turbulent Flow Simulation over Curved Surface: LES-WALE vs RANS Models Comparison

# overview

Comprehensive comparison of LES-WALE and RANS turbulence models performance for turbulent flow over curved geometry

Evaluate simulation accuracy in predicting flow separation

Analyze computational cost of each model

Investigate capability of predicting turbulent structures

Validate results with Greenblatt experimental data performance.

   # Geometry Specifications

Curved Hump Configuration

<img width="800" height="336" alt="image" src="https://github.com/user-attachments/assets/ea775575-99b0-494b-b831-d3c628c96957" />


# Computational Fluid Dynamics Approach
This study employs ANSYS Fluent as the primary CFD solver, utilizing its advanced turbulence modeling capabilities and robust numerical algorithms.
Software Configuration:

CFD Solver: ANSYS Fluent 2023 R1

Meshing Tool: ANSYS Meshing / ICEM CFD

Post-processing: ANSYS CFD-Post, Tecplot 360

Parallel Computing: MPI-based parallel processing
# Boundary Conditions
<img width="807" height="233" alt="image" src="https://github.com/user-attachments/assets/75fee7c6-0f08-48f0-8468-1afa0d519ee5" />


# Key Findings
Flow Physics Insights:

Separation Bubble Structure: LES-WALE captures unsteady vortex shedding accurately

Turbulent Kinetic Energy: RSM shows good agreement in peak TKE values

Wall Shear Stress: k-ω SST provides superior near-wall predictions

Pressure Distribution: LES-WALE matches experimental Cp curve most closely

