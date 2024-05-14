**Plot PCA, UMAP and tSNE**
===========================

We have already generated PCA, UMAP and tSNE embeddings for the dataset. However, it would be helpful to plot these embeddings and understand how our clusters look with different dimensionality reduction methods.

**For users running the workflow** -

* For the tSNE plot, scroll to the "Scanpy PlotEmbed" component of the workflow. All the values for parameters are default

* You can add a title under "Figure title". You can use the edit button next to other parameters to change the value

* For the UMAP plot, scroll to the second "Scanpy PlotEmbed" component of the workflow. All the values for parameters are default

* The third "Scanpy PlotEmbed" tool is for plotting the PCA. The same things as above apply here

**For users running each step** -

The first plot is the tSNE plot -

* For the tSNE plot, open up the tool "Scanpy PlotEmbed" and enter tsne under "name of the embedding to plot"

* Under "Field for gene symbols", enter Symbol

* You can add a title under "Figure title"

* You can change any other plot parameters that you would like to modify

* Click on "Execute"

The next plot to generate is the UMAP plot

* For the UMAP plot, open up the tool "Scanpy PlotEmbed" and enter umap under "name of the embedding to plot"

* Under "Field for gene symbols", enter Symbol

* You can add a title under "Figure title"

* You can change any other plot parameters that you would like to modify

* Click on "Execute"

The final plot to generate is the PCA plot

* For the PCA plot, open up the tool "Scanpy PlotEmbed" and enter pca under "name of the embedding to plot"

* Under "Field for gene symbols", enter Symbol

* You can add a title under "Figure title"

* You can change any other plot parameters that you would like to modify

* Click on "Execute"

Your PCA, tSNE, and UMAP plots are ready to be viewed. These plots reduce the dimensionality of your data, and you can peek at different clusters broadly in a lower dimension. PCA plot is not as helpful as UMAP and tSNE plots since the PCA plots, in general, could plot one PC against the other (mostly PC1 vs. PC2), like in Figure 1. UMAP and tSNE plots are most helpful and can provide more insight into the clusters, like their distribution, and also help determine if there is a batch effect. Batch effect is when we see that some samples have more expression of genes compared to some other samples. Let's look at some plots for PCA, tSNE and UMAP dimensioanlity reduction.

.. figure:: /images/PCA_clustering_labeled.png
   :width: 400
   :height: 400
   :alt: Principal components
   
   The PCA plot above only plots the first PC against the second PC and hence cannot capture the complexity of the data properly

Since PCA cannot capture the complexity of the data, it would be better to look at the UMAP and tSNE plots


.. figure:: /images/tSNE.png
   :width: 400
   :height: 400
   :alt: tSNE
   
   The tSNE plot above shows the 7 clusters that are obtained


.. figure:: /images/umap.png
   :width: 400
   :height: 400
   :alt: UMAP
   
   The UMAP plot above shows the 7 clusters that are obtained

The UMAP or tSNE plot can also be used to study batch effects in your data. For example, in the UMAP plot, you can see that the 








