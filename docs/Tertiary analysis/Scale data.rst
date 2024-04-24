**Scale data**
==============

Scaling data in single-cell analysis involves standardizing the expression levels of genes across all cells to have a uniform scale, typically achieving a mean of zero and a variance of one. This process, often referred to as z-score normalization, helps mitigate the effects of gene expression variability that are not relevant for distinguishing cell types or states. By scaling the data, researchers ensure that highly variable genes do not dominate the analysis, allowing for more accurate comparisons and integrations of datasets from different sources. Tools like Seurat and Scanpy include functions specifically designed for efficient scaling of single-cell RNA-seq data, which is pivotal for downstream analytical processes such as dimensionality reduction and clustering. 

In our workflow, we use the tool "Scanpy ScaleData" to scale the data.

**For users running the workflow** -

