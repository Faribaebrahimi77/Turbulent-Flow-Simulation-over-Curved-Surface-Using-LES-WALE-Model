# v6-LatestCopyPublishLES-WALE-vs-RANS-Turbulence-Models-Comparative-Analysis-for-Curved-Hump-Flow
Comparative study of LES-WALE vs RANS turbulence models for turbulent flow over a curved hump geometry using the Greenblatt experimental benchmark. Evaluates accuracy, computational cost, and predictive performance.


performance.
🏗️ Geometry Specifications

Hump Length (c): 420 mm
Maximum Height (h): 53.7 mm
Geometry Type: 2D profile extended in span-wise direction
Test Section Dimensions:

Height: 508 mm
Width: 711 mm
Splitter plate to ceiling: 382 mm
Model span: 584 mm


Non-dimensional Analysis: All lengths normalized by hump chord length (c)

🔬 Research Scope & Methodology
Flow Configuration

Flow Type: Steady-state time-averaged analysis (RANS) vs. Unsteady resolved simulation (LES)
Fluid: Incompressible turbulent flow
Geometry: Curved hump with strong adverse pressure gradient
Reference: Greenblatt experimental validation dataset
Reynolds Number: Re_c = 936,000 (based on hump chord length)

Turbulence Modeling Approaches
🌊 Large Eddy Simulation (LES-WALE)

Subgrid-Scale Model: Wall-Adapting Local Eddy-viscosity (WALE)
Resolution Strategy: Resolves large-scale turbulent structures directly
Near-Wall Treatment: WALE model adapts to wall proximity automatically
Grid Requirements: High-resolution LES mesh (y+ ≈ 1, Δx+ ≈ 50-100)
Time Integration: Unsteady solver with small time steps

🔄 RANS Models for Comparison

k-ε Standard Model
k-ε Realizable Model
k-ω SST Model
Spalart-Allmaras Model
Reynolds Stress Model (RSM)

🎯 Key Comparison Objectives
Accuracy Assessment

✅ Flow Separation Prediction: Location and extent of separation bubble
✅ Reattachment Point Accuracy: Comparison with experimental measurements
✅ Surface Pressure Distribution: Pressure coefficient validation
✅ Velocity Profiles: Boundary layer and wake characteristics
✅ Turbulent Statistics: Reynolds stresses, turbulent kinetic energy
✅ Unsteady Flow Features: Vortex shedding, flow instabilities (LES only)

Computational Performance

⚡ CPU Time Requirements: Wall-clock time comparison
⚡ Memory Usage: RAM requirements for each approach
⚡ Grid Resolution Needs: Mesh density requirements
⚡ Convergence Characteristics: Stability and robustness analysis
⚡ Parallel Scalability: Multi-core/cluster performance

🔬 Experimental Reference - Greenblatt et al.
Wind Tunnel Configuration:

Test Facility: Closed-loop wind tunnel
Reynolds Number: Re_c = 936,000 (based on hump chord)
Boundary Layer: Fully developed turbulent upstream condition
Measurement Techniques:

Particle Image Velocimetry (PIV)
Surface pressure taps
Hot-wire anemometry


Available Data: Surface Cp, velocity profiles, separation/reattachment points

📊 CFD Implementation Strategy
LES-WALE Simulation Setup

Solver: Unsteady, incompressible Navier-Stokes
Time Discretization: Second-order implicit scheme
Spatial Discretization: Bounded central differencing
Time Step: CFL ≈ 0.5-1.0 for temporal accuracy
Subgrid Model: WALE with automatic wall damping
Statistical Averaging: Time-averaged results over multiple flow-through times

RANS Simulation Setup

Solver: Steady-state, incompressible Reynolds equations
Pressure-Velocity Coupling: SIMPLE/PISO algorithm
Discretization: Second-order upwind schemes
Convergence: Residuals < 10^-6
Wall Treatment: Enhanced wall functions or low-Re formulations

Computational Domain & Boundary Conditions

Domain Extension: 5c upstream, 15c downstream, 3c height
Inlet: Turbulent velocity profile matching experiment
Outlet: Pressure outlet with zero gradient
Walls: No-slip condition on hump surface
Span-wise (LES): Periodic boundary conditions
Grid Strategy: Structured/hybrid mesh optimized for each method

📈 Expected Deliverables & Results
Comparative Analysis Results

Accuracy Comparison Matrix: Quantitative error analysis for each model
Surface Pressure Validation: Cp distribution vs. experimental data
Flow Field Visualization:

Time-averaged velocity contours (both methods)
Instantaneous vorticity fields (LES only)
Streamline patterns showing separation bubble


Turbulence Statistics Comparison: Reynolds stresses, TKE profiles
Computational Cost Analysis: CPU time vs. accuracy trade-off curves

Performance Metrics

Separation Point Accuracy: X/c location error analysis
Reattachment Point Prediction: Downstream recovery assessment
Peak Suction Coefficient: Maximum -Cp value and location
Pressure Recovery: Effectiveness in adverse pressure gradient region
Velocity Profile Matching: Boundary layer thickness and shape factors

Advanced LES Analysis

Unsteady Flow Phenomena: Vortex shedding frequency analysis
Spectral Analysis: Power spectral density of velocity fluctuations
Coherent Structures: Q-criterion isosurfaces and vortex identification
Intermittency Factor: Separation bubble unsteadiness quantification

🛠️ Software & Tools

LES Solver: OpenFOAM (pimpleFoam) / ANSYS Fluent
RANS Solver: ANSYS Fluent / OpenFOAM (simpleFoam)
Mesh Generation:

LES: High-resolution structured/hex mesh
RANS: Standard CFD mesh with boundary layer


Post-processing:

ParaView / Tecplot for visualization
Python/MATLAB for data analysis and statistics


HPC Resources: High-performance computing cluster for LES calculations

📚 Engineering Significance
Research Contributions

LES vs RANS Validation: Comprehensive comparison for separated flows
Computational Cost Assessment: Practical guidelines for method selection
Best Practices: Mesh requirements and solver settings optimization
Industrial Applications: Decision framework for turbulence modeling choice

Practical Applications

Airfoil Design: Accurate separation prediction for high-lift systems
Automotive Aerodynamics: Complex separated flow regions
Wind Energy: Blade stall characteristics and performance
HVAC Systems: Diffuser and bent duct flows
Marine Applications: Propeller and hull flow separation

📖 Key References

Greenblatt, D., et al. - Original experimental benchmark study
Nicoud, F. & Ducros, F. - WALE subgrid-scale model development
NASA TMR - Turbulence Model Resource validation cases
Pope, S.B. - Turbulent Flows (theoretical background)
