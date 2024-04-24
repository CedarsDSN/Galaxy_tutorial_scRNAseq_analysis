**Tertiary analysis**
=====================

Single-cell RNA sequencing (scRNA-seq) has emerged as a powerful tool for dissecting cellular heterogeneity and uncovering novel insights into biological systems with unprecedented resolution. Tertiary analysis of scRNA-seq data encompasses clustering, normalization, and related techniques and is crucial in transforming raw sequencing data into interpretable biological knowledge. The standard workflow for tertiary analysis of scRNA-seq data focuses on critical steps such as quality control, normalization, dimensionality reduction, clustering, and cell type identification. Normalization is an essential step for scRNA-seq data analysis, as it aims to remove technical biases and ensure comparability across cells and samples.

High-dimensional scRNA-seq data pose a challenge for visualization and interpretation. Dimensionality reduction techniques such as principal component analysis (PCA), t-distributed stochastic neighbor embedding (t-SNE), and uniform manifold approximation and projection (UMAP) are commonly used to reduce the dimensionality of the data while preserving its structure and capturing the main sources of variation. These techniques enable visualization of the data in two or three dimensions, facilitating the exploration of cell-to-cell relationships and the identification of distinct cell clusters.

Clustering algorithms are employed to partition cells into groups based on their gene expression profiles, enabling the identification of cell populations with similar transcriptional profiles. Standard clustering algorithms include k-means clustering, hierarchical clustering, and graph-based clustering. Once clusters have been identified, cell type identification involves annotating clusters with known cell types or states using marker genes or reference databases. Cell type annotation can be performed manually or using automated methods such as SingleR or CellAssign, which match cluster-specific gene expression profiles to reference datasets of known cell types.

Differential expression analysis is used to identify genes that are differentially expressed between cell clusters or experimental conditions, providing insights into the molecular signatures associated with specific cell types or states. Statistical methods such as the Wilcoxon rank-sum test or likelihood ratio test are commonly used to assess differential expression while accounting for technical variability and multiple testing. Genes that are significantly upregulated or downregulated in specific clusters can serve as candidate markers for characterizing cell types or elucidating biological processes.

Below are the steps for the tertiary analysis in our workflow -

.. toctree::

   Normalize data
   Find variable genes
   Scale data
   Run PCA and Build a neighborhood graph
   Run UMAP and tSNE
   Find clusters
   Find markers
   Plot PCA, UMAP and tSNE
   Annotate gene names in cluster file
