 # NEAS_Anchovy_Spawning_Grounds

This repository contains the data and code associated with the following publication:

**Characterizing spatiotemporal variability in anchovy spawning grounds: A case study from the North-East Aegean Sea (eastern Mediterranean)**

**Eleni Servou**<sup>1,2*</sup>, **Maxime Olmos**<sup>3</sup>, **Martin Huret**<sup>3</sup>, **Pierre Petitgas**<sup>4</sup>, **Eudoxia Schismenou**<sup>1,2</sup>, **Marianna Giannoulaki**<sup>2</sup> and **Stylianos Somarakis**<sup>2</sup>

<sup>1</sup> University of Crete, Biology Department, 70013, Heraklion, Crete, Greece

<sup>2</sup> Hellenic Centre for Marine Research (HCMR), Institute of Marine Biological Resources and Inland Waters (IMBRIW), 71003, Heraklion, Crete, Greece

<sup>3</sup> French Research Institute for Exploitation of the Sea (IFREMER), Ecosystem Dynamics and Sustainability (DECOD), 29280, Plouzané, France 

<sup>4</sup> French Research Institute for Exploitation of the Sea (IFREMER), Biological Resources and Environment (RBE), 44311, Nantes, France

**Corresponding author:** Eleni Servou ([e.servou@hcmr.gr](mailto:e.servou@hcmr.gr))

**DOI:** [To be added]

---

## Abstract

In dynamic ecosystems, understanding the spatiotemporal variability of fish spawning grounds is crucial for marine population ecology, as spawning habitat selection influences recruitment success and reflects ecosystem and population dynamics. However, disentangling the roles of environmental forcing and intrinsic population processes in shaping spawning distributions remains challenging.

This study analyzed available egg density data from the North-East Aegean Sea (NEAS), collected between 2003 and 2022, to investigate interannual variations in European anchovy (*Engraulis encrasicolus*) spawning grounds and to assess the influence of environmental and density-dependent processes on their spatiotemporal dynamics.

Using a spatiotemporal generalized additive mixed-effects modeling (GAMM) framework, we partitioned variability into stable spatial patterns, temporal variability, space–time interactions, and covariate effects. Environmental covariates were selected to represent the pronounced topographic, hydrological, and biological heterogeneity of the NEAS.

Spawning grounds exhibited strong spatial persistence, characterized by a stable spatial pattern with higher egg density over the continental shelf and lower density offshore. Bathymetry and sea surface salinity emerged as key drivers of spatial and spatiotemporal variability, while population biomass primarily accounted for temporal variability in egg density. The spatially varying effect of biomass revealed density-dependent spatial dynamics, consistent with the basin model theory.

Our findings indicate that anchovy spawning ground dynamics in the NEAS are driven by specific topographic and oceanographic features and biomass-dependent processes, while also highlighting the potential role of additional mechanisms, including behavioral processes such as spawning aggregation and site fidelity.

---

## Repository contents

The repository is organized as follows:

### 1. `data/`

This folder contains the data required for the analyses.

* **`data_glmm.xlsx`**
  Contains the observations used in the analyses, including the response variable (eggs0_abu), spatial and temporal information (Year, lon, lat), and covariate values (sal00_2to7m,sal00_2to7m,bottom_depth, TL_cm, Acoustic_Biomas, and CHL_extracted). 

  The data used in this study were collected within the framework of the Greek National Program for the Collection of Fisheries Data, co-funded by the Greek Ministry of Rural Development and Food and the European Union.

* **`Greece_geology.zip/`**
  Contains shapefiles representing:

  * the coastline of Greece (`Greece`);
  * rivers (`Rivers`);
  * isobaths (`Isobaths`).

  These spatial data were used to construct the barrier mesh and for visualization and mapping purposes.

### 2. `sdmTMB_NEAS_Anchovy_spawning_grounds.qmd`

Quarto document containing the code used to fit and compare the spatiotemporal models presented in the study.

### 3. `NEAS_barrier_mesh_sensitivity_analysis.qmd`

Quarto document containing the code used to perform the sensitivity analysis for optimizing the characteristics of the barrier mesh. The corresponding results are presented in Supplementary Material S2 of the paper.

---

## Software and packages

The analyses were performed in **R version 4.5.1** using the following package versions:

* `sdmTMB` v0.7.4
* `sdmTMBextra` v0.0.4

Other R packages used are specified within the code files.

---

## Data use and restrictions

The data provided in this repository were collected as part of the Greek National Program for the Collection of Fisheries Data (co-funded by the Greek Ministry of Rural Development and Food and the European Union) and are made available for the purpose of reproducing the analyses presented in the associated publication. 
