# Caspase-1 self-terminates protease activity to enforce homeostasis and prevent inflammasome-driven diseases

This repository contains the code and documentation for the study.

## Authors
Sabrina Sofia Burgener<sup>1†</sup>, Mark Thomas Milner<sup>1*</sup>, Shoumit Dey<sup>2*</sup>, Pooranee Morgan<sup>3</sup>, Daniel G Blackmore<sup>4</sup>, Emmanuelle Frampton<sup>1</sup>, Gregory Miller<sup>5,6</sup>, Monalisa Durate de Oliveira<sup>1</sup>, Kirsten Mayra Kenney<sup>1</sup>, Rinie Bajracharya<sup>1</sup>, Ulrich Baumgartner<sup>7</sup>, Albert Xiong<sup>1,8</sup>, Quan Nguyen<sup>1,8</sup>, Liviu-Gabriel Bodea<sup>4</sup>, Andrew Clouston<sup>5,6</sup>, Dave Boucher<sup>9</sup>, Juergen Goetz<sup>4</sup>, Andrew Murphy<sup>3</sup>, Paul M Kaye<sup>2</sup>, Kate Schroder<sup>1,10†</sup>

<sup>1</sup> Institute for Molecular Bioscience and IMB Centre for Inflammation and Disease Research, The University of Queensland, St Lucia 4072, Australia.  
<sup>2</sup> Hull York Medical School and York Biomedical Research Institute, University of York, York, UK.  
<sup>3</sup> Baker Institute, Melbourne, Australia  
<sup>4</sup> Clem Jones Centre for Aging and Dementia Research, Queensland Brain Institute, St. Lucia, Queensland, Australia.  
<sup>5</sup> Envoi Specialist Pathologist, Kelvin Grove 4059, Australia  
<sup>6</sup> Faculty of Medicine, The University of Queensland, Herston 4006, Australia  
<sup>7</sup> School of Biomedical Sciences, The University of Queensland, St Lucia 4072, Australia  
<sup>8</sup> Cell and Molecular Biology Department, QIMR Berghofer MRI, Herston 4006, Queensland, Australia  
<sup>9</sup> Department of Biology and York Biomedical Research Institute, University of York, York, UK.  
<sup>10</sup> Lead editorial contact  

<sup>*</sup> These authors contributed equally  
<sup>†</sup> Corresponding authors: s.burgener@uq.edu.au, k.schroder@uq.edu.au

## Summary

Signal shutdown mechanisms must exist to silence the potent inflammatory programs initiated by the caspase-1 (CASP1) protease, to allow inflammation to resolve and reinstate tissue homeostasis. This study investigates how CASP1 terminates its activity *in vivo* using a knock-in mouse model with a CASP1 CARD domain linker (CDL) mutation that prevents self-cleavage (*Casp1.CDL* mice). 

The research shows that CASP1 CDL autoproteolysis terminates CASP1 activity in vivo, and examines these mice under homeostatic conditions and in response to major physiological challenges affecting the brain, bone marrow, and liver. Key findings include:

1. In the brain, CASP1 CDL mutation caused anxiety-like behavior under homeostatic conditions, and exacerbated hippocampal spatial learning deficits in the *APP23* genetic model of amyloid-induced neurodegeneration.
2. In the bone marrow, CASP1 CDL mutation promoted steady-state granulopoiesis.
3. In a model of diet-induced liver disease, CASP1 CDL mutation accelerated liver steatosis and promoted liver immune cell infiltration, inflammation, and damage.
4. In a liver healing model, CASP1 CDL mutation delayed disease resolution, indicating that CASP1 autocleavage is required to restore homeostasis after a major challenge to organ function.

This research reveals that CASP1 CDL self-cleavage terminates CASP1 inflammatory programs *in vivo* to maintain homeostasis in steady-state, restore homeostasis after a major challenge to organ function, and suppress inflammasome-driven diseases.

## System Requirements

### OS
- Windows: Windows 10 x64 (recommended)
- Mac
- Linux (e.g., CentOS, Ubuntu)

### Software
- R (≥4.2.2)
- RStudio (optional)
- Python (≥3.8 for spatial transcriptomics integration via cell2location)

### Key R packages required:
- Seurat (≥4.3.0)
- ggplot2
- dplyr
- patchwork
- corrplot
- reshape2

## Repository Structure

### Primary Analysis Scripts

- `analysis_SD23.9.1_realigned.Rmd`: Main analysis script for Seurat-based spatial transcriptomics processing
- `analysis_cell2ocation_SD23.9.1_realigned.Rmd`: Analysis script for cell2location integration

### Data Sources

The repository relies on several data sources:
- Spatial transcriptomics (Visium) data processed with Space Ranger (v1.3.0)
- Cell type deconvolution using cell2location (v0.1) with reference single-cell dataset GSE129516
- Metadata for experimental conditions with four groups: healthy, caspase1, mc_def (methionine-choline deficient diet), and mc_def_caspase1

## Workflow Overview

1. **Data Loading and Pre-processing**
   - Loading 10X Visium data
   - Quality control and filtering
   - Metadata integration

2. **Normalization and Integration**
   - SCTransform normalization
   - Feature selection and anchor identification
   - Data integration across samples

3. **Clustering and Visualization**
   - Dimension reduction (PCA, t-SNE, UMAP)
   - Spatial visualization of clusters

4. **Differential Expression Analysis**
   - Cluster marker identification
   - Group-based differential expression
   - Expression analysis of specific immune-related genes

5. **Cell Type Deconvolution and Spatial Analysis**
   - Integration with reference scRNA-seq data
   - Cell2location for spatial mapping of cell types
   - Correlation analysis to determine spatial co-location of different cell types
   - Analysis of resident vs. infiltrating macrophages and their relationship to hepatocytes

## Running the Analysis

1. Clone this repository
2. Install required R packages
3. Set working directory to the repository root
4. Run the R markdown files in sequence

## Contact and Correspondence
- Sabrina Sofia Burgener: s.burgener@uq.edu.au
- Kate Schroder: k.schroder@uq.edu.au
- Shoumit Dey (data/code inquiries): shoumit.dey@york.ac.uk / shoumit@gmail.com

## License
This project is covered under the MIT License.
