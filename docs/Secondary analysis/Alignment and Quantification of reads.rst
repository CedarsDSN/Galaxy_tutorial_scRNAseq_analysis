**Alignment and Quantification of reads**
=========================================

Now that we have finished conducting the quality control. We are now ready to align the reads and then quantify these reads to obtain a count matrix. We use the RNA STARsolo tool for demultiplexing, alignment, and quantification. 

StarSolo is a robust module for measuring gene expression in single-cell and single-nucleus RNA-seq data. Integrated into the widely-used RNA-seq aligner STAR (Spliced Transcripts Alignment to a Reference), StarSolo excels in accuracy and speed, surpassing many other tools that use pseudoalignment-to-transcriptome methods.

The module efficiently handles tasks such as read mapping, assigning reads to genes, demultiplexing cell barcodes, and collapsing UMIs (Unique Molecular Identifiers). Its integrated approach minimizes input/output delays and boosts processing efficiency. Unlike some tools that only align reads to the transcriptome, StarSolo performs alignments to the entire genome, enhancing the accuracy of the results.

**For users of the workflow:**

* Expand the "Demultiplexing, Alignment and Quantification" component of the workflow that has the arguments for the parameters for the RNA STarsolo tool

* You can use the default parameters or input your own parameters by using the edit button next to the tool in question

* One thing that is important to note here is that the default reference genome here is human (hg38 index). If your reads are from different organisms, you can use the edit button and choose from Drosophila melanogaster (dm6 sequence index), Mus musculus (mm10 sequence index) or Rattus norvegicus (rat sequence index)

**For users running each step of the workflow**

* Open up the "RNA STARsolo" tool by searching in the tool list on the left-hand side

* Provide the paired collection of the input dataset you created and also the whitelist of the cell barcodes for your data. If you don't have one, please use these `instructions <https://galaxy-tutorial-landing-page.readthedocs.io/en/latest/Miscellaneous/Obtaining%20files%20from%20Data%20Libraries.html>`_ to access a data library to access the list that we have available

* You can use the default parameters or input your own parameters by using the drop-down menu for each parameter

* You are ready to run the tool once all arguments are entered

MultiQC can be run on RNA STARsolo output and is optional. To run MultiQC -

* Under "Results" > "Insert Results" > select "STAR" for "Which tool was used to generate logs?"

* In "STAR output" > "Insert STAR output" > "Type of STAR output > "Log"

* Select your STAR log output - "RNA STAR on collection N: log" 


