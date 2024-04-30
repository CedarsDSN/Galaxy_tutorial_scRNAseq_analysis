**Annotate gene names in cluster file**
=======================================

As you have gone through the tutorial till this stage, you would have noticed that the gene symbols are used as the field when plotting tSNE, UMAP and PCA plots. We prefer the gene names in the final cluster file for ease of use, so we don't have to re-check what symbols match which genes. The AnnData format we use in this workflow already has the gene names stored in the object, which we need to extract. We will use a tool to extract the specific table with the gene annotation information and then use join and cut tools to obtain the final table with cluster information for each generated cluster.

**For users running the workflow** -

* Scroll down to the three tools "Inspect AnnData", "Join two datasets" and "Cut"

* You don't need to change any values for the parameters. You are now ready to run the workflow

* Scroll to the top of the page and click "Run Workflow"

**For users running each step** -

The first step is to obtain the annotation information from the AnnData object

* Open up the tool "Inspect AnnData" and select the output of "Scanpy FindMarkers" as the input object

* Under "What to inspect", select "Key-indexed annotation of variables/features (var)"

* Click on "Execute"

The second step is to join the table from above with the table from "Scanpy FindMarkers"

* Search for the tool "Join two Datasets"

* Under "Join", select the tabular output from the "Scanpy FindMarkers" tool

* Under "using column", enter 4

* Under "with", select the tabular output from the "Inspect AnnData" tool

* Under "and column", enter 2

* Under "Keep lines of first input that do not join with second input", select Yes

* Under "Keep lines of first input that are incomplete", select Yes

* Under "Fill empty columns", select No

* Under "Keep the header lines", select Yes

* Click on "Execute"

The third step is to cut unnecessary columns and only retain the ones we need and in the right order

* Open the tool "Cut columns from a table" from the search toolbar

* Under "Cut columns", enter "c1,c2,c3,c4,c11,c5,c6,c7,c8"

* Under "Delimited by", select Tab

* Provide the dataset from the "Join two Datasets"

* Click on "Execute"

You are now done with Single-cell tertiary analysis and ready to look at your clusters and markers within them.
