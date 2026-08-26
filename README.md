# AlxCoCrFeNi Atomistic Simulations

Atomistic simulation workflows for studying the mechanical, thermal, vibrational, and microstructural behavior of AlxCoCrFeNi high-entropy alloys using molecular dynamics simulations.

---

## Overview

This repository presents the computational work from my undergraduate research on **Al<sub>x</sub>CoCrFeNi high-entropy alloys (HEAs)**, with the Al content varied over the range: **0.1 ≤ x ≤ 0.7**

The work mainly uses **molecular dynamics (MD) simulations in LAMMPS** to study how composition and atomic-scale structure influence different material properties.

Atomistic Simulations:

* Uniaxial tensile deformation
* Generalized stacking fault energy (GSFE)
* Lattice thermal conductivity
* Phonon density of states (PDOS)
* Mean-square displacement (MSD)
* Polycrystalline structure generation using Voronoi tessellation

Python/Jupyter Notebook scripts are included for representative post-processing and visualization.

The purpose of this repository is to organize the computational work in a **clear, reproducible, and accessible form** rather than to provide the complete raw simulation dataset.

---

## Undergraduate Thesis

**Title:**
*Fundamental Investigation of the Tensile Behavior and Lattice Thermal Conductivity of AlxCoCrFeNi (0.1 ≤ x ≤ 0.7) High Entropy Alloys: An Atomistic Study*

**Degree:**
B.Sc. in Mechanical Engineering

**Institution:**
Khulna University of Engineering & Technology (KUET), Bangladesh

**Research Area:**
Computational Materials Science / Physical Metallurgy / High-Entropy Alloys

The thesis focuses on understanding composition-dependent mechanical and thermal behavior of Al<sub>x</sub>CoCrFeNi alloys from an atomistic perspective.

In addition to the principal tensile and thermal-conductivity investigations, complementary atomistic analyses were performed to examine defect energetics, atomic mobility, and vibrational behavior.

More recently, the computational workflow has also been extended toward **polycrystalline structure generation and grain-boundary-related modeling** using Voronoi tessellation.

---

## Research Objectives

The main objectives of this computational work are to:

1. Investigate the influence of Al concentration on the tensile response of Al<sub>x</sub>CoCrFeNi HEAs.

2. Examine atomistic deformation behavior through stress-strain simulations.

3. Evaluate generalized stacking fault energy and obtain insight into the energetics associated with crystallographic slip.

4. Investigate lattice thermal transport behavior using molecular dynamics simulations.

5. Analyze atomic vibrational characteristics through phonon density of states calculations.

6. Examine atomic mobility using mean-square displacement analysis.

7. Develop computational workflows for generating polycrystalline atomic structures using Voronoi tessellation.

8. Build a structured and reproducible atomistic-simulation workflow that can be extended to future studies of complex alloys, phase stability, grain-boundary effects, and multiscale materials modeling.

---

## Computational Work

The computational work represented in this repository includes the development, modification, and organization of simulation and post-processing workflows for the following tasks:

* Atomic structure preparation
* LAMMPS simulation setup
* Energy minimization
* Thermal and pressure equilibration
* Uniaxial deformation
* Stress-strain data extraction
* Generalized stacking fault calculations
* Thermal-property simulations
* PDOS analysis
* MSD analysis
* Data post-processing using Python
* Scientific visualization
* Polycrystalline structure generation using Atomsk
* Voronoi tessellation for grain construction

The repository contains **demonstration versions** of input files and representative data so that the overall methodology can be understood without requiring the complete large-scale simulation datasets.

---



## Simulation Workflows

### 1. Uniaxial Tensile Simulation

The tensile workflow examines the mechanical response of AlxCoCrFeNi HEAs under uniaxial deformation.
It is used to study how alloy composition affects the stress-strain response and related mechanical behavior at the atomic scale.  

The general workflow consists of:

1. Atomic structure preparation
2. Assignment of atomic species
3. Interatomic potential selection
4. Energy minimization
5. Thermal and pressure equilibration
6. Application of controlled uniaxial deformation
7. Stress calculation
8. Stress-strain data extraction
9. Python-based post-processing and visualization


---

### 2. Generalized Stacking Fault Energy

The GSFE workflow studies the change in energy caused by the relative displacement of atomic planes along a selected crystallographic slip direction.

This analysis helps examine defect-related behavior and the resistance of the crystal structure to slip.

Generalized stacking fault calculations provide useful atomistic information about:

* Slip energetics
* Stable and unstable fault configurations
* Resistance to crystallographic shearing
* Composition-dependent deformation behavior

The workflow generally involves:

1. Construction of the required crystal orientation
2. Definition of the fault/slip plane
3. Incremental displacement of part of the structure
4. Energy minimization
5. Extraction of system energy
6. Calculation of excess fault energy
7. Construction of the GSFE curve


---

### 3. Lattice Thermal Conductivity

The lattice thermal-conductivity workflow uses molecular dynamics to study heat transport in AlxCoCrFeNi alloys.

The main goal is to understand how changes in composition and atomic-scale disorder influence thermal transport.

The workflow includes simulation setup, equilibration, thermal-property calculations, data extraction, and post-processing. The corresponding workflow folder contains the simulation details and parameters used in the research.



---

### 4. PDOS and MSD Analysis

Two complementary atomistic analyses are included in this workflow.

#### Phonon Density of States

Phonon density of states describes the distribution of vibrational modes in the simulated material.

The PDOS analysis is used to examine atomic vibrations and how changes in alloy composition affect the vibrational behavior of the HEA system.

#### Mean-Square Displacement

Mean-square displacement measures how far atoms move, on average, from their initial positions as the simulation progresses.

The MSD analysis is used to examine atomic mobility and how atomic motion changes under different simulation conditions.

MSD analysis is useful for examining:

* Atomic mobility
* Temperature-dependent atomic motion
* Diffusive behavior
* Dynamical characteristics of the atomic system


---

### 5. Polycrystalline Structure Generation

The polycrystalline workflow represents an extension of the atomistic modeling work toward the investigation of **grain-boundary and grain-size effects**.

Polycrystalline atomic structures are generated using **Atomsk** and Voronoi tessellation.

A representative workflow is:

```text
Create FCC unit cell
        ↓
Define simulation box
        ↓
Generate random grain seeds
        ↓
Apply Voronoi tessellation
        ↓
Generate polycrystalline atomic structure
        ↓
Wrap atoms into simulation box
        ↓
Import structure into LAMMPS
        ↓
Relax/equilibrate structure
        ↓
Perform subsequent MD analysis
  
```

  
---
## Software and Tools

The primary computational tools used in this project are:

### LAMMPS

**Large-scale Atomic/Molecular Massively Parallel Simulator**

Used for:

* Molecular dynamics simulations
* Energy minimization
* Structural equilibration
* Mechanical deformation
* Defect-energy calculations
* Thermal-property simulations
* Atomic trajectory generation

Website: https://www.lammps.org/

---

### Atomsk

Used for:

* Atomic structure generation
* Crystal manipulation
* Polycrystalline model construction
* Voronoi tessellation

Website: https://atomsk.univ-lille.fr/

---

### Python

Used for:

* Numerical data processing
* Analysis of simulation output
* Calculation of derived quantities
* Scientific visualization

Representative Python packages used in the post-processing workflows include:

* NumPy
* pandas
* Matplotlib
* Jupyter


---

### Jupyter Notebook

Used to provide transparent, step-by-step post-processing workflows in which calculations, explanations, data processing, and plots can be viewed together.

---

### OVITO

Used for visualization and inspection of atomistic simulation structures and trajectories.

Website: https://www.ovito.org/

---

## Interatomic Potential

The accuracy of molecular dynamics simulations strongly depends on the interatomic potential used to describe interactions among Al, Co, Cr, Fe, and Ni atoms.

The potential used in the thesis simulations should be documented using the following information:

* **Potential name:** `FeNiCrCoAl-heaweight.setfl`
* **Potential type:** `eam/alloy`
* **Original authors:** `D. Farkas, and A. Caro (2020)`
* **Publication:** `Model interatomic potentials for Fe–Ni–Cr–Co–Al high-entropy alloys", Journal of Materials Research 35, 3031-3040.`
* **DOI:** `(https://doi.org/10.1557/jmr.2020.294)`
* **Potential source:** `(https://www.ctcms.nist.gov/potentials/system/Al-Co-Cr-Fe-Ni/)`


```

The interatomic-potential file itself is **not included in this repository unless redistribution is explicitly permitted by its original source or license**.

Users attempting to reproduce the simulations should obtain the appropriate potential directly from the original authorized source and update the relevant path in the LAMMPS input scripts where necessary.

```


## Reproducibility

My undergraduate thesis has not yet been published, so the full LAMMPS input scripts, simulation data, and detailed results are not publicly available at this stage.

I will update this section with the relevant scripts, data, and results once the work is published. 

    
---


## LAMMPS

Plimpton, S. (1995). Fast Parallel Algorithms for Short-Range Molecular Dynamics. *Journal of Computational Physics, 117*(1), 1–19.
DOI: https://doi.org/10.1006/jcph.1995.1039

---

## Atomsk

Hirel, P. (2015). Atomsk: A tool for manipulating and converting atomic data files. *Computer Physics Communications, 197*, 212–219.
DOI: https://doi.org/10.1016/j.cpc.2015.07.012

---

## OVITO

Stukowski, A. (2010). Visualization and analysis of atomistic simulation data with OVITO—the Open Visualization Tool. *Modelling and Simulation in Materials Science and Engineering, 18*(1), 015012.
DOI: https://doi.org/10.1088/0965-0393/18/1/015012

---

## High-Entropy Alloys

Cantor, B., Chang, I. T. H., Knight, P., & Vincent, A. J. B. (2004). Microstructural development in equiatomic multicomponent alloys. *Materials Science and Engineering: A, 375–377*, 213–218.
DOI: https://doi.org/10.1016/j.msea.2003.10.257

Yeh, J.-W., Chen, S.-K., Lin, S.-J., Gan, J.-Y., Chin, T.-S., Shun, T.-T., Tsau, C.-H., & Chang, S.-Y. (2004). Nanostructured high-entropy alloys with multiple principal elements: Novel alloy design concepts and outcomes. *Advanced Engineering Materials, 6*(5), 299–303.
DOI: https://doi.org/10.1002/adem.200300567

---

## Interatomic Potential
  
D. Farkas, and A. Caro (2020), "Model interatomic potentials for Fe–Ni–Cr–Co–Al high-entropy alloys", Journal of Materials Research 35, 3031-3040. DOI: 10.1557/jmr.2020.294.

  

---
## Author of This GitHub Repository

**Sourov Ahmed**

B.Sc. in Mechanical Engineering.  
Khulna University of Engineering & Technology (KUET), Khulna, Bangladesh.  
---
  
**Research interests:**

* Computational Materials Science
* Physical Metallurgy
* High-Entropy Alloys
* Molecular Dynamics
* Computational Thermodynamics
* Phase Stability
* CALPHAD
* Microstructure Modeling

The main purpose of this repository is to present my undergraduate computational materials research and the related work I am continuing in atomistic and multiscale materials modeling.

---
**GitHub:**
https://github.com/Sourov-Ahmed-2005034

---

### Repository Status

The repository is still being organized and documented. I am preparing the simulation workflows as clear, reproducible examples while keeping the original research data protected and respecting any restrictions on third-party computational resources.

---
