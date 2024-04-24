**Scale data**
==============

Scaling data in single-cell analysis involves standardizing the expression levels of genes across all cells to have a uniform scale, typically achieving a mean of zero and a variance of one. This process, often referred to as z-score normalization, helps mitigate the effects of gene expression variability that are not relevant for distinguishing cell types or states. By scaling the data, researchers ensure that highly variable genes do not dominate the analysis, allowing for more accurate comparisons and integrations of datasets from different sources. Tools like Seurat and Scanpy include functions specifically designed for efficient scaling of single-cell RNA-seq data, which is pivotal for downstream analytical processes such as dimensionality reduction and clustering. 

In our workflow, we use the tool "Scanpy ScaleData" to scale the data.

**For users running the workflow** -

* In the workflow, you don’t need to enter any values. All values are default. Use the edit button next to the parameter you would like to change. You are ready to move on to the next step

**For users running each step** -

* Open the tool “Scanpy ScaleData”

* Under "Truncate to this value after scaling", enter 10.0

* All other parameters are default

* Click on “Execute”
