**Run PCA and Build a neighborhood graph**
==========================================

Principal Component Analysis (PCA) is a statistical method commonly used in data analysis to identify patterns in high-dimensional data by transforming it into a new coordinate system. In the context of single-cell RNA sequencing (scRNA-seq), where each cell's gene expression profile is captured, PCA plays a crucial role in reducing the dimensionality of the data while retaining most of its variability. This reduction simplifies data visualization and facilitates the identification of biologically relevant features, such as cell types or states, amidst the complexity of gene expression profiles. By condensing the information into principal components, which are orthogonal axes representing the directions of maximum variance, PCA enables researchers to uncover underlying cellular heterogeneity, identify rare cell populations, and characterize dynamic biological processes, thereby advancing our understanding of complex biological systems at the single-cell level. When we get to the clustering step, the PCA plot helps determine the number of dimensions to use for clustering.

Building a neighborhood graph, mainly through methods like k-nearest neighbor (kNN) or shared nearest neighbor (SNN) algorithms, is an integral step in single-cell RNA sequencing (scRNA-seq) analysis. These graphs represent relationships between individual cells based on similarities in their gene expression profiles. By connecting cells that are close neighbors in gene expression space, these graphs capture the underlying structure of the cellular population, revealing clusters, trajectories, and transitions between cell states. Constructing such graphs enables the exploration of cell-cell interactions, identification of rare cell populations, and inference of developmental trajectories or cellular transitions. Additionally, these graphs serve as the foundation for downstream analysis techniques like graph-based clustering and trajectory inference, facilitating the interpretation of complex biological systems at single-cell resolution. In our workflow, the ComputeGraph tool uses k-nearest neighbor algorithm.

**For users using the workflow** -

* Under "Scanpy RunPCA" tool, the default number of PCs to produce is 50. If you want to increase this number, use the edit button next to "Number of PCs to produce" and modify it to the number you choose. 

* Under "ScanPy ComputeGraph" tool, the default value for "Maximum number of neighbors used" is 15 and the default "Number of PCs to use" is 50. Both of these numbers can be changed by using the edit button and modifying it to a number of your choice

**For users running each step** -

The first step is to run PCA using the "ScanPy RunPCA". Open the tool by using the search tool on the left hand-side

* Select the scaled AnnData/Loom formatted dataset outputted by the last tool

* Under "Number of PCs to produce", select the number of PCs you would like to be produced

* Make sure "Zero center data before scaling" is set to Yes

* Click on "Execute"

The second step is to compute the KNN graph using the "ScanyPy ComputeGraph" tool. Open the tool by searching for it in the search toolbar

* Open the tool and provide the AnnData/Loom dataset under input object

* Set "Use programme defaults" to No and change the defaults to your choice. The main arguments to change are the "Maximum number of neighbors used" and the "Number of PCs to use". The defaults for these two are 15 and 50 respectively

* Click on "Execute"


