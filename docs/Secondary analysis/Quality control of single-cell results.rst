**Quality control of single-cell results**
==========================================

In Single-cell RNA-seq analysis, it's very important to conduct the quality control and filtering steps to make sure we have true cells with genes with true transcripts. Our goal here is to **filter** the data to only include true cells that are of high quality, so that when we cluster our cells it is easier to identify distinct cell type populations.
Further, we also want to identify any failed samples and either try to salvage the data or remove from analysis, in addition to, trying to understand why the sample failed. The main challenges are delineating cells that are poor quality from less complex cells, and choosing appropriate thresholds for filtering, so as to keep high quality cells without removing biologically relevant cell types. 

The important metrics that you will encounter in any single-cell RNA-seq analysis are as follows -

* nCount_RNA (Seurat) or total_counts (Scanpy): Total number of UMIs per cell

* nFeature_RNA (Seurat) or n_genes_by_counts (Scanpy): Total number of genes with counts in a cell

* mito.percent (Seurat) or pct_counts_mt (Scanpy): Percentage of cell reads originating from the mitochondrial genes

Some metrics are specific to Scanpy. The ones that you would be using to understand and filter your data are -

* log1p_genes_by_counts: the logarithmic value of the value n_genes_by_counts

* log1p_total_counts: the logarithmic value of the value total_counts

* n_cells: 




