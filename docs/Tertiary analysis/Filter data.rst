**Filter data**
===============

In the previous section, we studied each important metric for single-cell RNA-seq analysis in detail. We also looked at how each scatter plot and violin plot would look depending on which filter you use and the thresholds therein. Understanding the metrics is essential to handling your data better. No two datasets are the same, and it's important to understand your data. 

**For users running the workflow** -

* Navigate to "Workflows" and then "Single-cell RNA-seq tertiary analysis" workflow and click on the "Run workflow" button. Under Input AnnData, select your AnnData formatted object from your history. If you want to understand how to import your data from 

* The previous section goes into the default values of the three metrics under "Filtering by Features", "Filtering by Counts", and "Filtering by percentage of mitochondrial counts". If you would like to modify the default values according to the scatter plots for your data, use the edit button to change the Min value and Max value under each of these three headings

* Unfortunately, the violin plots generated after running each filtering step will show up after the whole workflow is run. If you want to see what each of the filters does to your data in terms of violin plot, you should run each filter separately and plot the violin plot after applying each filter (as explained below under "For users running each step")

* One last filter before we move on to the next step is "Filtering cells". We want to ensure that genes that do not appear in any cell or just 1-2 cells are removed. Under "Filtering cells", the "Min value" is set to three and "Max value" is set to a very large number. Three is a conservative number; you can use the edit button to increase it to 10 or so.

**For users running each step** -

* The tertiary analysis starts with filtering the data. We filter using the three metrics that were introduced in the earlier section

* The first filter filters by features (features being genes here). Open up the tool "Scanpy FilterCells" and under "Name of parameter to filter on", enter "log1p_n_genes_by_counts". Provide the AnnData object for your data. If you have run the primary analysis, the scatter plots generated there will help you determine the thresholds to set under "Min value" and "Max value." If you haven't run the primary analysis, you can generate your own scatter plots using the instruction `here <https://galaxy-tutorial-scrnaseq-analysisgalaxy-tutorial-scrnaseq-analy.readthedocs.io/en/latest/Secondary%20analysis/Quality%20control%20of%20single-cell%20results.html>`_. To understand how to interpret the scatter plots, refer to this `section <https://galaxy-tutorial-scrnaseq-analysisgalaxy-tutorial-scrnaseq-analy.readthedocs.io/en/latest/Tertiary%20analysis/Brief%20tutorial%20on%20filtering%20data.html>`_. Click on "Execute". You can then plot the violin plot using "Plot using Scanpy" and provide the variables to plot.

* The second filter filters by counts. Open up the tool "Scanpy FilterCells" and under "Name of parameter to filter on", enter "log1p_total_counts" and enter the "Min value" and "Max value". The scatter plots can help you determine the thresholds here again. You can go ahead and either look at your scatter plots or create them using instructions through the link mentioned above and interpret them using the same. Click on "Execute". You can then plot the violin plot using "Plot using Scanpy" and provide the variables to plot.

* The third filter filters by percentage of mitochondrial counts. Open up the tool "Scanpy FilterCells" and under "Name of parameter to filter on", enter "pct_counts_mito" and enter the "Min value" and "Max value" by examining the scatter plots. Click on "Execute". You can then plot the violin plot using "Plot using Scanpy" and provide the variables to plot.

* The fourth filter filters by number of cells that a feature (gene) expresses in. Open up the tool "Scanpy FilterGenes" and under "Name of parameter to filter on", enter "n_cells" and enter the "Min value" and "Max value" by examining the scatter plots. Click on "Execute".

* You have now finished filtering and are ready to move to the next step.
