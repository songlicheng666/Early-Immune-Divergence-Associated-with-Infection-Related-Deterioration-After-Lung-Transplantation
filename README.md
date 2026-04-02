# Single-Cell and BCR Analysis Pipeline

This repository contains an analysis workflow for longitudinal single-cell RNA-seq and B-cell receptor repertoire data.

## Project goals

The project aims to:

- process and integrate multi-sample scRNA-seq datasets
- annotate major immune cell populations
- perform subclustering of major lineages
- analyze dynamic changes in cell composition over time
- characterize B-cell, neutrophil, monocyte, and T-cell functional states
- integrate BCR repertoire data with scRNA-seq
- evaluate clonotype structure, isotype usage, and somatic hypermutation

## Project structure

- `scripts/01_preprocessing`: raw data loading, QC, integration, PCA
- `scripts/02_major_celltype_annotation`: major lineage annotation and proportions
- `scripts/03_subclustering`: subclustering of NEU, MON, B, and T cells
- `scripts/04_bcell_analysis`: B-cell-specific analyses
- `scripts/05_neutrophil_analysis`: neutrophil-specific analyses
- `scripts/06_monocyte_analysis`: monocyte-specific analyses
- `scripts/07_bcr_analysis`: BCR repertoire analysis and integration

## Main analysis modules

1. Seurat object creation and merging
2. QC metric calculation and filtering
3. Data normalization and integration
4. Sample-level pseudo-bulk PCA
5. Major cell type annotation
6. Cell composition analysis
7. Subclustering of major immune lineages
8. B-cell functional analysis
9. Neutrophil functional analysis
10. Monocyte functional analysis
11. BCR clonotype and SHM analysis

## Requirements

Main R packages include:

- Seurat
- dplyr
- ggplot2
- patchwork
- Harmony
- scRepertoire
- immunarch
- UCell
- ComplexHeatmap
- clusterProfiler
- msigdbr
- ggpubr

## Notes

- Raw data paths in the original scripts were local and should be updated before running.
- Some analyses were initially performed at the cell level and may require adaptation to sample-level pseudobulk statistics for publication-grade differential testing.
- Large plotting and exploratory scripts have been reorganized into analysis-specific modules.

## Contact

Please open an issue if you have questions about the workflow.
