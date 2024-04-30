**Find clusters**
=================

Clustering is a fundamental step in analyzing single-cell RNA sequencing (scRNA-seq) data, essential for identifying distinct cell populations and understanding their heterogeneity. Through clustering, cells with similar gene expression profiles are grouped, revealing underlying biological structures such as cell types, subtypes, and states. Various clustering algorithms, including graph-based approaches like Louvain or hierarchical clustering methods, are employed to partition cells into clusters based on similarities in their gene expression patterns. These clusters serve as a basis for characterizing cell populations, elucidating cell lineage relationships, and identifying rare or transitional cell states within heterogeneous cell populations. Clustering also facilitates downstream analyses such as differential expression analysis, cell type annotation, and trajectory inference, enabling researchers to gain insights into cellular ecosystems' functional and regulatory diversity with unprecedented resolution and depth.

In our workflow, we will be using the Louvian algorithm.

**For users running the workflow** - 

* The tool that conducts clustering in the workflow is "ScanyPy FindCluster"

* Under this tool, you can change the clustering algorithm from Louvian to Leiden

* Under "Resolution, high value for more and smaller clusters", the default value is 0.6 and you can change the value using the edit button nect to the parameter

**For users running each step** -

* Open the tool "ScanPy FindCluster" using the search tool

* Select the output of the earlier tool from history under "Input object"

* Select No under “Use programme defaults”

* Here you can change the values to all parameters suitable to your choice. The important parameter is "Resolution, high value for more and smaller clusters" whose default value is 1.0 but can be changed to a value of your choice

* Click on "Execute"
