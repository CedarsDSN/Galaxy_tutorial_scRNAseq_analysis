**Alignment and Quantification of reads**
=========================================

Now that we have finished conducting the quality control. We are now ready to align the reads and then quantify these reads to obtain a count matrix. We use the RNA STARsolo tool for demultiplexing, alignment, and quantification. 

StarSolo is a robust module for measuring gene expression in single-cell and single-nucleus RNA-seq data. Integrated into the widely-used RNA-seq aligner STAR (Spliced Transcripts Alignment to a Reference), StarSolo excels in accuracy and speed, surpassing many other tools that use pseudoalignment-to-transcriptome methods.

The module efficiently handles tasks such as read mapping, assigning reads to genes, demultiplexing cell barcodes, and collapsing UMIs (Unique Molecular Identifiers). Its integrated approach minimizes input/output delays and boosts processing efficiency. Unlike some tools that only align reads to the transcriptome, StarSolo performs alignments to the entire genome, enhancing the accuracy of the results.
