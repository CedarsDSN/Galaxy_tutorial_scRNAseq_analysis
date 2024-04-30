**Find markers**
================

In single-cell RNA sequencing (scRNA-seq) analysis, identifying marker genes is crucial for characterizing distinct cell populations and understanding their functional roles within complex biological systems. Marker genes are those whose expression levels are significantly associated with specific cell types or states. Various statistical methods, such as differential expression analysis using algorithms like DESeq2 or edgeR, are employed to identify differentially expressed genes between different cell clusters or conditions. Additionally, specialized tools like SCENIC or Seurat's FindMarkers function offer tailored approaches for marker gene discovery in scRNA-seq data. Once identified, marker genes serve as signatures for defining cell types, subtypes, or states, providing insights into cellular identity, function, and regulatory networks. They are invaluable for understanding cellular heterogeneity, developmental trajectories, and disease states, thereby advancing our knowledge of complex biological processes at the single-cell level.

We will use Scanpy's "Find Markers" function to find differentially expressed genes.

**For users running the workflow** -

* The tool that computes the differentially expressed genes is "ScanPy FindMarkers"

* Under this tool, you can change parameters such as "The sample grouping/clustering to use" from Louvain to Leiden, and also, the "Number of top genes to show per cluster" can be altered. The default is 50

**For users running each step** -

* Open the tool "ScanPy FindMarkers" using the search toolbar

* You can change parameters such as "The sample grouping/clustering to use" from Louvain to Leiden, and also, the "Number of top genes to show per cluster" can be altered. The default is 50

* You can also alter additional parameters by selecting No under “Use programme defaults”. It shows you additional parameters

* Click on "Execute"
