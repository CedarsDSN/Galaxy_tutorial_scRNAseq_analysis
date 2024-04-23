**Quality check**
=================

We will be using FASTQC tool to conduct a quality check of our files. FastQC is designed to offer an easy method for performing quality control evaluations on raw sequencing data derived from high-throughput sequencing technologies. It features a series of modular analyses that help quickly determine if there are any significant issues with your data that you need to address before proceeding with more in-depth analysis.

**For users of the workflow** - let's start with the "Single-cell RNA-seq Primary analysis" workflow. 

* From the homepage, navigate to "Workflow" and scroll down to "Single-cell RNA-seq Primary analysis"

* Provide the collection of fastq files that you created in the previous step from the dropdown menu under "Input dataset collection". This step is just providing input to the tools within the workflow

* Also, you can upload the whitelist of cell barcodes that you would like to use

* The tool that will run the first step i.e. Quality check is FastQC and you don't have to provide any values under FastQC. We will be using the default values

**For users running each step** - 

* The paired dataset collection created in the previous step can be provided to the tool - FastQC

* Find FastQC in the toolshed on the left side and launch the tool

* Provide the dataset you uploaded to the FastQC tool and run the tool


Output of FastQC -


HTML file can be viewed after downloading it from the history. Below are all the information and plots that one can expect from the FastQ HTML report -

* Basic statistics - This is precisely what it says: all basic statistics about your fastq samples, which include but are not limited to the total number of sequences, sequence length, and GC%

* Various plots showing per sequence quality scores, per base sequence content, per sequence GC content, per base N content, sequence duplication levels, and adapter content. One of the plots below shows the per-base sequence quality

* If you would like more information on interpreting each of the plots and statistics in the FastQC output, `this <https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon/lessons/qc_fastqc_assessment.html>`_ is an excellent place to start. Scroll down to the "Analysis quality metrics" to look at the interpretation of each plot.
