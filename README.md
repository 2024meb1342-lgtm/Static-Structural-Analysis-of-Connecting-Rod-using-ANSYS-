Static Structural Analysis of a Connecting Rod using ANSYS
Project Overview

This project presents the static structural analysis of an internal combustion engine connecting rod using ANSYS Mechanical 2019 R1. The primary objective is to evaluate the structural performance of the connecting rod under static loading conditions by determining the equivalent (von Mises) stress, equivalent elastic strain, and total deformation. The study identifies critical stress concentration regions and verifies whether the connecting rod operates safely within the material's elastic limit.

Objectives
Design a 3D connecting rod model using CAD software.
Perform finite element analysis (FEA) using ANSYS Mechanical.
Apply realistic boundary conditions and loading.
Evaluate stress, strain, and deformation distributions.
Identify critical regions prone to stress concentration.
Visualize structural behavior through deformation and stress animations.
Software Used
SolidWorks 2021 – CAD Modeling
ANSYS Workbench 2019 R1
ANSYS Mechanical
Static Structural Analysis Module
Material
Grey Cast Iron
Property	Value
Density	7200 kg/m³
Young's Modulus	110 GPa
Poisson's Ratio	0.28
Tensile Strength	200 MPa
Compressive Strength	820 MPa
Yield Strength	Brittle Material (Yield strength not typically defined)

Note: Grey cast iron is a brittle material. Therefore, failure is generally assessed using tensile strength or brittle failure criteria rather than yield strength.

Methodology
1. CAD Modeling

The connecting rod was modeled in SolidWorks, including:

Small end
Big end
Shank
Oil hole
Fillets

The completed model was exported to ANSYS for structural analysis.

2. Material Assignment

Grey Cast Iron was assigned as the material in ANSYS Engineering Data, and all relevant mechanical properties were defined.

3. Mesh Generation

A tetrahedral finite element mesh was generated.

To improve result accuracy, a finer mesh was created around:

Fillets
Oil hole
Transition regions

These locations are expected to experience higher stress concentrations.

4. Boundary Conditions
Big End: Fixed Support
Small End: Static load applied to simulate the piston force transmitted through the connecting rod.
5. Solver

A linear static structural analysis was carried out under the following assumptions:

Linear elastic material behavior
Small deformation
Static loading
Room temperature
No thermal effects
Results
Equivalent (Von-Mises) Stress

Maximum Stress

78.34 MPa

The highest stress occurs near:

The transition between the shank and the big end
Around the oil hole

These are common stress concentration locations in connecting rods due to geometric discontinuities.

Equivalent Elastic Strain

Maximum Equivalent Elastic Strain

7.12 × 10⁻⁴

The highest strain is observed around:

Oil hole
Fillet region
Shank transition

The strain values indicate elastic deformation under the applied loading.

Total Deformation

Maximum Total Deformation

0.258 mm

The maximum deformation occurs near the loaded small end of the connecting rod, while the fixed big end shows negligible displacement.

Discussion

The finite element analysis shows that the connecting rod experiences maximum stress in the fillet and oil-hole regions due to stress concentration. The stress distribution follows the expected load path from the small end to the big end through the shank. The deformation is relatively small and remains within the elastic range assumed for the analysis.

Since the maximum equivalent stress (78.34 MPa) is significantly lower than the tensile strength of grey cast iron (approximately 200 MPa), the connecting rod is expected to safely withstand the applied static load under the assumptions of this analysis.

Conclusion

A static structural analysis of a connecting rod made from Grey Cast Iron was successfully performed using ANSYS Mechanical.

The analysis produced the following key results:

Result	Value
Maximum Equivalent Stress	78.34 MPa
Maximum Equivalent Elastic Strain	7.12 × 10⁻⁴
Maximum Total Deformation	0.258 mm

The maximum stress is below the material's tensile strength, indicating that the connecting rod can safely sustain the applied static loading conditions. The highest stresses occur near the fillet and oil-hole regions, highlighting these areas as critical locations for design consideration.

Project Files
Connecting-Rod-Static-Analysis/
│
├── CAD Model/
│   ├── ConnectingRod.SLDPRT
│   └── ConnectingRod.STEP
│
├── ANSYS/
│   ├── ConnectingRod.wbpj
│   ├── Solver Files
│   └── Engineering Data
│
├── Results/
│   ├── Equivalent_Stress.png
│   ├── Equivalent_Strain.png
│   ├── Total_Deformation.png
│
├── Animations/
│   ├── Stress_Animation.mp4
│   ├── Strain_Animation.mp4
│   └── Deformation_Animation.mp4
│
└── README.md
