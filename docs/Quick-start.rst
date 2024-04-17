Quick-start
============

**Primary analysis workflow (includes Primary and Secondary analysis)**

This is the list of steps that one would require to run the “Single-cell RNA-seq Primary analysis” workflow without getting into too much detail about each step. To understand each step in-depth, please proceed to the next page.


1. Open Galaxy and sign in with your username and password 
2. Create a new history for this analysis and rename this history with a name that is intuitive to you
3. Next, since this is a tutorial for single-cell RNA-seq reads from 10X, the reads for a particular would look like this - 
  a. pbmc_1k_v3_S1_L001_R1_001.fastq.gz
  b. pbmc_1k_v3_S1_L001_R2_001.fastq.gz
  c. pbmc_1k_v3_S1_L001_I1_001.fastq.gz
4. The package CellRanger requires all three files. The following pages go into more detail about these files. We will only need the files with suffixes _R1 and _R2 for this workflow. The package RNA STARsolo doesn't need the _I1 file. 
5. Upload the _R1 and _R2 files that you would like to run the Single-cell RNA-seq analysis with and create a paired collection (Instructions are `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20data.html>`_) If you would like to use an example dataset, please use these detailed `instructions <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Using%20example%20data.html>`_. 
6. If your files are larger than 10 GB, consider using FTP, the instructions of which are `here <https://galaxy-tutorial-landing-page.readthedocs.io/en/latest/Miscellaneous/Importing%20large%20data.html>`_
7. Navigate to the "Workflows" tab on the top of the Galaxy homepage
8. Next to the workflow named "Single-cell RNA-seq Primary analysis", click on the start button
9. This will navigate you to the page to enter all the values to run this workflow. Here, you can either send all the output to the current history or make a new history
10. Another file that you will need is the whitelist of known cell barcodes, which are extracted from the CellRanger pipeline. This file is provided to you under the data library in Galaxy. Please download it and upload it under History. Instructions to access the data library can be found `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Supplementary%20files/Obtaining%20files%20from%20Data%20Libraries.html>`_
11. Currently, the workflow is set up to take a collection of paired samples - R1 and R2. To create a paired collection using your samples, use this set of instructions. Once you upload and create your samples, create a paired collection that will show up in your history. Select this collection under "Input dataset collection"
12. Under "Cell Barcode file", select the previously uploaded whitelist of known cell barcodes from the history
13. Under "Demultiplexing and Quantification", the tool being used is RNA STARsolo. The default reference genome in our workflow is the mouse genome. To select from a list of reference genomes, click on the Edit button next to "Select reference genome" and choose the reference genome of your choice from the drop-down list
14. All the arguments are set to default for the "RNA STARsolo" tool. You can change the parameters for any of the arguments using the edit button
15. The following tool is "DropletUtils" which helps filter the RNA STARsolo output using various filtering parameters. Under DropletUtils, there is default filtering applied. If you would like to change these filters, please use the edit button next to the filter you are interested in and modify it
16. For the multiQC report, the user doesn't need to enter any arguments
17. The following tool is "Scater: Calculate QC metrics" where the filtered dataset is redirected. It creates a SingleCellLoomExperiment dataset, which can be redirected to the next tool, "Scater: plot library QC"
18. The tool "Scater: plot library QC" plots the QC metrics for the data. The tool is set to not plot on a log scale, but you can modify that according to what you would like
19. Click the "Run Workflow" button at the top to run the workflow


**Tertiary analysis workflow (includes Tertiary analysis)**

1. For the "Single-cell RNA-seq tertiary analysis" workflow, you would either run it after the Primary Analysis workflow and use the Loom dataset (please refer to `this <https://galaxy-tutorial.readthedocs.io/en/latest/Tertiary%20analysis/Importing%20data/Importing%20count%20data%20from%20Primary%20Analysis.html>`_ page) or run it on your own dataset (please refer to `this <https://galaxy-tutorial.readthedocs.io/en/latest/Tertiary%20analysis/Importing%20data/Importing%20example%20data%20for%20running%20Tertiary%20Analysis.html>`_ page)
2. Navigate to the workflows tab, and select the Run button for the “Single-cell RNA-seq tertiary Analysis” workflow to open the workflow and choose the dataset that you would like to use
3. 

