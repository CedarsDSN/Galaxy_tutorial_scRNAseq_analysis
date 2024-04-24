**Normalize data**
==================

Normalizing single-cell data is a crucial step in single-cell analysis, aimed at removing technical noise and ensuring comparability across cells. This process typically involves adjusting for differences in library size and detecting variability across the cells. Methods such as TPM (Transcripts Per Million), CPM (Counts Per Million), and normalization using scaling factors like those from the scran package in R, help to standardize the data before downstream analyses. These normalized datasets are then used to accurately identify gene expression patterns, cellular heterogeneity, and biological signaling pathways specific to single-cell studies.

We use the tool "Scanpy NormalizeData" in this workflow "Tertiary analysis of Single-cell RNA-seq" to normalize our single-cell RNA-seq dataset.

**For users running the workflow** -

* Open up the workflow and provide your AnnData dataset to the workflow

* The first step is normalizing data. You don't need to enter any arguments here. You can move on to the next step

**For users running each step** -

* In the tools, look for "Scanpy NormalizeData" and provide your AnnData dataset in "Input object"

* All other parameters are default. Click on "Execute"
