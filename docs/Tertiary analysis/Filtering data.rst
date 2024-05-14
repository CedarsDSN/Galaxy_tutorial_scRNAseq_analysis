**Filtering data**
==================

In single-cell RNA sequencing (scRNA-seq) analysis, several key metrics are used during quality control (QC) filtering to assess the data quality. Among these, the number of unique molecular identifiers (nUMI), the total number of counts (nCounts), and the percentage of mitochondrial gene expression (nMitopercent) are particularly important.

**nUMI (Number of Unique Molecular Identifiers)**
nUMI represents the number of unique RNA molecules captured and sequenced per cell. This metric helps to determine the complexity and depth of the sequencing. Cells with very low nUMI may indicate poor quality or insufficient sequencing depth, while excessively high nUMI can suggest potential doublets or other artifacts. Proper thresholding of nUMI ensures that only cells with a sufficient and realistic number of unique transcripts are included in the analysis.

**nCounts (Total Number of Counts)**
nCounts refers to the total number of RNA transcripts detected in each cell, including all UMI counts. It provides a measure of the overall transcriptional activity within a cell. Similar to nUMI, cells with extremely low nCounts might be of low quality, while those with excessively high nCounts may be suspect for artifacts like doublets. Filtering based on nCounts helps exclude cells that do not meet the expected levels of transcriptional activity, thus ensuring data quality.

**nMitopercent (Percentage of Mitochondrial Gene Expression)**
nMitopercent indicates the proportion of total RNA transcripts derived from mitochondrial genes. A high percentage of mitochondrial gene expression can be a sign of cellular stress or apoptosis, as stressed or dying cells often show elevated levels of mitochondrial RNA. By setting a threshold for nMitopercent, cells with unusually high mitochondrial content can be filtered out, improving the overall quality of the dataset.

**Combining Metrics for Effective QC**
Together, these metrics provide a comprehensive view of cell quality. Researchers can effectively filter out poor-quality cells by analyzing and applying appropriate thresholds for nUMI, nCounts, and nMitopercent, leading to a more reliable and accurate scRNA-seq dataset. Visual tools, such as scatter plots and violin plots, are often used to visualize these metrics and assist in setting appropriate cutoffs for filtering. This rigorous QC process is crucial for ensuring the validity of downstream analyses and obtaining meaningful biological insights.
