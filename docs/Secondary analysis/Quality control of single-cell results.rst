**Quality control of single-cell results**
==========================================

In Single-cell RNA-seq analysis, we must conduct the quality control and filtering steps to ensure we have actual cells with genes with accurate transcripts. Our goal here is to **filter** the data only to include high-quality true cells so that when we cluster our cells, it is easier to identify distinct cell type populations.
Further, we also want to identify any failed samples and either try to salvage the data or remove them from analysis and try to understand why the sample failed. The main challenges are delineating cells of poor quality from less complex cells and choosing appropriate thresholds for filtering to keep high-quality cells without removing biologically relevant cell types. 

The critical metrics that you will encounter in any single-cell RNA-seq analysis are as follows -

* nCount_RNA (Seurat) or total_counts (Scanpy): Total number of UMIs per cell

* nFeature_RNA (Seurat) or n_genes_by_counts (Scanpy): Total number of genes with counts in a cell

* mito.percent (Seurat) or pct_counts_mt (Scanpy): Percentage of cell reads originating from the mitochondrial genes

Some metrics are specific to Scanpy. The ones that you would be using to understand and filter your data are -

* log1p_genes_by_counts: the logarithmic value of the value n_genes_by_counts

* log1p_total_counts: the logarithmic value of the value total_counts

* n_cells: the count of the number of cells a particular gene appears in

Once alignment is done, the tools "DropletUtils", "Scater: Calculate QC metrics" and "SCEasy Converter" are used. "DropletUtils" converts the tsv output format from RNA STARsolo to tabular format. "Scater: Calculate QC metrics" converts the tabular format to Loom format. Finally, the "SCEasy Converter" tool converts loom to AnnData format, which Scanpy uses. 

**For users that are running the workflow** -

* You don't have to enter any values here

**For users that are running each step** -

* You can look for the "DropletUtils" tool in the tools section and provide the output from the "RNA STARsolo" tool. Click on "Execute"

* For the following tool, "Scater: Calculate QC metrics", provide the output from the "DropletUtils" tool. Click "Execute"

* The tool "SCEasy Converter" - select "Loom to AnnData" and provide the loom output data from the "Scater: Calculate QC metrics" tool






