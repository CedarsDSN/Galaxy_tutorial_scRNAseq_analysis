
**Primary analysis**
====================

For single-cell RNA-seq analysis, Primary analysis is the first crucial step in understanding the transcriptomic data gathered from single-cell RNA sequencing. This process involves converting raw sequencing data into a form that can be further analyzed to uncover the rich biological insights hidden within. It sets the foundation for all subsequent analyses and interpretations. Single-cell RNA sequencing generates multiple read files, and they are labeled as R1, R2, R3 (or I1). These are the standard files produced but can vary depending on the technology and the sequencer. 

* R1 has the Barcode information
* R2 typically has the actual cDNA sequences
* I1 is typically from an illumina sequencer and will contain the Illumina lane information

Demultiplexing is a crucial initial step in the processing of next-generation sequencing (NGS) data, especially when samples are multiplexed during sequencing. Multiplexing allows multiple samples to be sequenced simultaneously in a single sequencing run by tagging each DNA or RNA fragment from different samples with unique sequence tags known as barcodes or indices. Demultiplexing is the process of sorting these mixed reads back into their original sample groups based on these barcodes, effectively identifying and separating sequences that belong to different samples. The most common tool that is used for demultiplexing is Illumina's bcl2fastq. Demultiplexing is an essential step in ensuring that sequencing data is properly organized and attributed to the correct samples for accurate analysis in any multi-sample sequencing experiment. Once demultiplexing is done, the next step is conducting the alignment and quantification to get a count matrix. 

We use the "RNA STARsolo" tool for our workflow to carry out demultiplexing and quantification. Before conducting this, we need to conduct quality control of the fastq files. 

