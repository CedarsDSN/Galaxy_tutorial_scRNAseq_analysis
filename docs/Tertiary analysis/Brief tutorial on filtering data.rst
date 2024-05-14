**Brief tutorial on filtering data**
====================================

In single-cell RNA sequencing (scRNA-seq) analysis, several key metrics are used during quality control (QC) filtering to assess the data quality. Among these, the number of unique molecular identifiers (nUMI), the total number of counts (nCounts), and the percentage of mitochondrial gene expression (nMitopercent) are particularly important.

**nFeature_RNA (Number of Unique Molecular Identifiers)**
nFeature_RNA represents the number of unique RNA molecules captured and sequenced per cell. This metric helps to determine the complexity and depth of the sequencing. Cells with very low nFeature_RNA may indicate poor quality or insufficient sequencing depth, while excessively high nFeature_RNA can suggest potential doublets or other artifacts. Proper thresholding of nFeature_RNA ensures that only cells with a sufficient and realistic number of unique transcripts are included in the analysis.

**nCount_RNA (Total Number of Counts)**
nCount_RNA refers to the total number of RNA transcripts detected in each cell, including all UMI counts. It provides a measure of the overall transcriptional activity within a cell. Similar to nFeature_RNA, cells with extremely low nCount_RNA might be of low quality, while those with excessively high nCount_RNA may be suspect for artifacts like doublets. Filtering based on nCount_RNA helps exclude cells that do not meet the expected levels of transcriptional activity, thus ensuring data quality.

**nMitopercent (Percentage of Mitochondrial Gene Expression)**
nMitopercent indicates the proportion of total RNA transcripts derived from mitochondrial genes. A high percentage of mitochondrial gene expression can be a sign of cellular stress or apoptosis, as stressed or dying cells often show elevated levels of mitochondrial RNA. By setting a threshold for nMitopercent, cells with unusually high mitochondrial content can be filtered out, improving the overall quality of the dataset.

**Combining Metrics for Effective QC**
Together, these metrics provide a comprehensive view of cell quality. Researchers can effectively filter out poor-quality cells by analyzing and applying appropriate thresholds for nUMI, nCounts, and nMitopercent, leading to a more reliable and accurate scRNA-seq dataset. Visual tools, such as scatter plots and violin plots, are often used to visualize these metrics and assist in setting appropriate cutoffs for filtering. This rigorous QC process is crucial for ensuring the validity of downstream analyses and obtaining meaningful biological insights.

In our workflow, we can look at the scatter plots from the primary workflow and use that to determine thresholds for the three metrics above. 

First, it would be better to interpret the scatter plots from the primary workflow and then use that to demonstrate what thresholds will be chosen to filter the data. Look at the scatter plot under "Scatter - mito x genes". This is plotting the nFeature_RNA against nMitopercent (The notation is a bit different. log1p_n_genes_by_counts is nFeature_RNA and pct_counts_mito is nMitopercent). You can also use a violin plot to determine a threshold, but scatter plots are helpful. Below is an example of such a scatter plot.

.. figure:: /images/scatter_mito_genes.png
   :width: 400
   :height: 400
   :alt: UMAP
   
   Fig 1: Scatter - mito x genes

The above plot shows how cells with log1p_n_genes_by_count (nFeature_RNA) up to 5.7-5.8 often have high pct_counts_mito. We can set 5.7 as a lower limit when filtering. Let's keep the max value as 20.0. In the tertiary workflow, under the "Filtering by features", the default value is 5.7 for "Min value" and 20.0 for "Max value". You should check your scatter plot and interpret it to obtain a threshold. After filtering, we can look at violin plots comparing the raw data and after applying this filter. 

.. figure:: /images/raw_vs_first_filter.png
   :width: 400
   :height: 400
   :alt: UMAP
   
   Fig 2: Raw data vs the first filter - genes/cell

Now, we can move to the next metric. Look at the scatter 