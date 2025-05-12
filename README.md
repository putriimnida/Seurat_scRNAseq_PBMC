# Seurat v5: scRNA-seq Analysis of PBMCs (2,700 cells)

This repository documents my learning journey and practice using the Seurat v5 package for single-cell RNA sequencing (scRNAseq) data analysis. The project includes preprocessing, dimensionality reduction, clustering, and identification of cell-type-specific markers. The dataset analyzed consists of 2,700 Peripheral Blood Mononuclear Cells (PBMCs) made publicly available by 10X Genomics, following the official Seurat v5 tutorial.


## 📘 Tutorial Reference ##
[Seurat v5 - Getting Started with PBMCs](https://satijalab.org/seurat/articles/get_started_v5_new)

## 🧬 Dataset ##
Source: [10X Genomics PBMC 2.7k dataset](https://support.10xgenomics.com/single-cell-gene-expression/datasets/1.1.0/pbmc3k)<br>
Description: a scRNA-seq dataset of 2,700 PBMCs

## 🛠️ Workflow Summary ##
1. **Seurat Object Setup & Data Loading**
   - Read PBMC 10X dataset using `Read10X`
   - Created a Seurat object with `CreateSeuratObject`
2. **Quality Control**
   - Calculated:
     - Number of features (genes)
     - Total counts
     - Percentage of mitochondrial gene expression
   - Visualized distributions and applied filters
3. **Normalization and Feature Selection**
   - Log-normalized the data
   - Identified variable features with `FindVariableFeatures`
4. **Dimensionality Reduction**
   - PCA performed on scaled data
   - Visualized PCA loadings and explored important PCs using `DimHeatmap()`
5. **Clustering and visualization**
   - Constructed nearest neighbor graph and performed clustering
   - UMAP used to visualize cell clusters in 2D space
6. **Marker Gene Identification**
   - `FindAllMarkers()` used to detect cluster-specific genes
   - Plotted marker expression using violin and feature plots
  
## 🧰 Packages Used
- `Seurat`
- `ggplot2`
- `dplyr`
- `patchwork`
- `ggrepel`


## 📘  How to Run the Notebook

1. Clone the repository:
   ```bash
   git clone https://github.com/putriimnida/Seurat_scRNAseq_PBMC.git
   cd Seurat_scRNAseq_PBMC
