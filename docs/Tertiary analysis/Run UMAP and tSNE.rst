**Run UMAP and tSNE**
=====================

Uniform Manifold Approximation and Projection (UMAP) is a dimensionality reduction technique that has emerged as a powerful tool in analyzing single-cell RNA sequencing (scRNA-seq) data. Unlike traditional methods such as t-distributed stochastic neighbor embedding (t-SNE), UMAP preserves both global and local structure in the data, allowing for a more accurate representation of complex biological relationships. By transforming high-dimensional gene expression profiles into a lower-dimensional space, UMAP enables visualization of cellular heterogeneity, identification of distinct cell populations, and exploration of continuous cellular trajectories. Its ability to capture non-linear relationships and preserve local neighborhood structures makes UMAP well-suited for revealing subtle biological variations and dynamics within heterogeneous cell populations. Moreover, UMAP embeddings serve as a foundation for downstream analyses such as clustering, trajectory inference, and cell type identification, thus playing a crucial role in advancing our understanding of cellular heterogeneity and dynamics in diverse biological systems.

t-distributed Stochastic Neighbor Embedding (t-SNE) is a widely used dimensionality reduction technique in single-cell RNA sequencing (scRNA-seq) analysis. It is particularly valued for its ability to reveal intricate relationships within high-dimensional data. By modeling pairwise similarities between cells in high-dimensional space and optimizing a low-dimensional representation to reflect these similarities best, t-SNE effectively maps cells with similar gene expression profiles close together in the visualization. This property makes it invaluable for visualizing complex biological structures such as cell types, subtypes, and developmental trajectories. Although t-SNE is computationally intensive and sensitive to its hyperparameters, its ability to capture non-linear relationships and highlight rare cell populations makes it an indispensable tool for exploring the rich diversity and dynamics of cellular landscapes in scRNA-seq datasets. Moreover, t-SNE embeddings serve as a foundation for downstream analyses such as cell clustering, differential expression analysis, and identification of regulatory networks, contributing significantly to our understanding of cellular heterogeneity and function.

We will be using the workflow to run both UMAP and t-SNE

**For users running the workflow** -

* Under the tools "ScanPy RunTSNE", all default values have been set for the different parameters

* You can change the different parameters to your choice using the edit button next to each parameter

* The same applies for the tool to run UMAP under "ScanPy RunUMAP"

**For users running each step** -

The first step is to run tSNE using the “ScanPy RunTSNE”. Open the tool by using the search tool on the left-hand-side

* Select the AnnData/Loom formatted dataset (output of the earlier tool) as input dataset

* Under "Use programme defaults", select No

* Here, you can change the values given to tool parameters such as the perplexity, tightness within and between clusters and the learning rate. You can also add additional parameters such as the the number of jobs and number of PCs to use

* Click on "Execute"

The second step is to run UMAP using the "ScanPy RunUMAP" tool. Use the search tool to open it

* Select the output of the earlier tool as input here

* Select No under "Use programme defaults"

* Here you can change the values to all parameters suitable to your choice. Parameters such as Initial learning rate, effective spread of embedded points, etc.

* Click on "Execute"




