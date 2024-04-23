**Secondary Analysis**
======================

At this stage, you have looked at the quality of your reads; they are ready to be aligned to a genome in order to assess which genes they originate from. However, the genome is not always available and has to use a reference genome, a representative example of the set of genes in a particular species. However, one must keep in mind that these genes do not accurately represent all the sets of genes in one organism. They act as a skeleton on which new genomes are built. For alignment in this tutorial, RNA STARsolo is used. It can align the single-cell reads to a reference genome and output BAM files, which can then be provided to the quantification tool, which can output a gene level count matrix, which can be used for downstream analysis.

If you would like to learn in-depth about single-cell RNA-seq, these `tutorials <https://training.galaxyproject.org/training-material/topics/single-cell/>`_ developed by Galaxy which goes into each step and explains along with examples. Most of the tutorials have example data which you can use when running the tutorial.


.. toctree::

   Alignment and Quantification of reads
   Quality control of single-cell results
   Accessing results
