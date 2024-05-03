Single-cell RNA-seq introduction
================================

Single-cell RNA-seq analysis is a swiftly advancing field at the forefront of transcriptomic research. It's widely used in studies focused on developmental processes and rare transcripts, allowing researchers to explore the diversity of cells within a population with unprecedented detail. This method offers a unique combination of cellular resolution and genome-wide coverage, enabling the discovery of new previously inaccessible insights using traditional bulk RNA-seq techniques.

However, analyzing single-cell RNA-seq data has its challenges. It requires a solid understanding of statistics, wet-lab protocols, and some familiarity with machine-learning techniques due to the inherent variability and sparsity of the data. In the past, low coverage and limited cell numbers per sample posed significant obstacles in the field, leading to uncertainties in the results.

Fortunately, the emergence of technologies like 10x Genomics has revolutionized single-cell RNA-seq analysis by providing high-throughput solutions. These advancements have rapidly propelled the field forward, overcoming previous limitations and paving the way for new discoveries.

===========

This tutorial goes through the steps of single-cell RNA-Seq analysis mentioned below and is based on a Galaxy `tutorial <https://training.galaxyproject.org/training-material/topics/single-cell/tutorials/scrna-case_basic-pipeline/tutorial.html>`_ -  
  - Primary analysis 
      * Using example data
      * Importing data
      * Quality check
  - Secondary analysis
      * Alignment and Quantification of reads
      * Quality control of single-cell results
  - Tertiary analysis
      * Normalize data
      * Find variable genes
      * Scale data
      * Run PCA and Build a neighborhood graph
      * Run UMAP and tSNE
      * Find clusters
      * Find markers
      * Plot PCA, UMAP and tSNE
      * Annotate gene names in cluster file
  - Conclusion
