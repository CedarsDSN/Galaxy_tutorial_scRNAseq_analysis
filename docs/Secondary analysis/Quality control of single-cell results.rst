**Quality control of single-cell results**
==========================================

In Single-cell RNA-seq analysis, it's very important to conduct the quality control and filtering steps to make sure we have true cells with genes with true transcripts. Our goal here is to **filter** the data to only include true cells that are of high quality, so that when we cluster our cells it is easier to identify distinct cell type populations.
Futher, we also want to identify any failed samples and either try to salvage the data or remove from analysis, in addition to, trying to understand why the sample failed. 

