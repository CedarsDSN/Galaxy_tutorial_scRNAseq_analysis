Quick-start
============

Primary analysis workflow (includes Primary and Secondary analysis)

This is the list of steps that one would require to run the “Single-cell RNA-seq Primary analysis” workflow without getting into too much detail about each step. To understand each step in-depth, please proceed to the next page.


1. Open Galaxy and sign in with your username and password 
2. Create a new history for this analysis and rename this history with a name that is intuitive to you
3. Next, since this is a tutorial for single-cell RNA-seq reads from 10X, the reads for a particular would look like this - 
  a. pbmc_1k_v3_S1_L001_R1_001.fastq.gz
  b. pbmc_1k_v3_S1_L001_R2_001.fastq.gz
  c. pbmc_1k_v3_S1_L001_I1_001.fastq.gz
4. The package CellRanger requires all three files. The following pages go into more detail about these files. We will only need the files with suffixes _R1 and _R2 for this workflow. The package RNA STARsolo doesn't need the _I1 file. 
5. Upload the _R1 and _R2 files that you would like to run the Single-cell RNA-seq analysis with (Instructions are `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20data.html>`_) If you would like to use an example dataset, please use these detailed `instructions <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Using%20example%20data.html>`_. 
6. Under "Create a collection of input files", select your collection of fastq files from the dropdown menu. To create a collection of your fastq files, refer to the steps on `this <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20large%20data.html>`_ page. If your files are larger than 10 GB, consider using FTP, the instructions of which are `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20large%20data.html>`_
7. Navigate to the "Workflows" tab on the top of the Galaxy homepage
8. Next to the workflow named "Single-cell RNA-seq Primary analysis", click on the start button
9. This will navigate you to the page to enter all the values to run this workflow. Here, you can either send all the output to the current history or make a new history
10. Another file that you will need is the whitelist of known cell barcodes, which are extracted from the CellRanger pipeline. This file is provided to you under the data library in Galaxy. Please download it and upload it under History. Instructions to access the data library can be found `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Supplementary%20files/Obtaining%20files%20from%20Data%20Libraries.html>`_
11. Currently, the workflow is set up to take files from 2 samples. For selecting samples -
  a. Under Sample 1 Read 1, select the R1 file from Sample 1
  b. Under Sample 1 Read 2, select the R2 file from Sample 1
  c. Under Sample 2 Read 1, select the R1 file from Sample 2
  d. Under Sample 2 Read 2, select the R2 file from Sample 2
12. The default reference genome in this workflow is the mouse genome. To select from a list of reference genomes, click on the Edit button next to "Select reference genome" and choose the reference genome of your choice from the drop-down list
13. For the "RNA STARsolo" tool, all the arguments are default

