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
