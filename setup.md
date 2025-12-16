# Setup


## Steps
1.  Create a workspace called `Graph Tutorial`  
Make sure your workspace is connected to a Fabric Capacity.
2.  Create a lakehouse called `lh_graph`.  
  Do **not** enable Lakehouse schema.  It is not currently compatible with Graph in Fabric.

> [!CAUTION]
> Do **not** enable Lakehouse schema.  It is not currently compatible with Graph in Fabric.

3.  Import the notebook `Notebook Graph Tutorials.ipynb` from the notebooks folder in the repo into the workspace:

![Upload Files](/images/importNotebook.png)

4.  Open the notebook and attach it to your new lakehouse
- Attach the Lakehouse by clicking **Add data items** > **Existing data sources** inside the Notebook

5.  Click **Run all** on the notebook
6.  If the notebook does not complete successfully, debug it or work with your instructor until it does

## Exercises
- Inspect the notebook code.  Can you think of another way to do it?
- Observe the way the the data modelling is done in the code, using mapping tables, nodes and edges
- Inspect the tables in the Lakehouse Explorer.
- Write some SQL queries against the new tables using the SQL Endpoint


## Next Steps
[Lab 01 - Numbers](/labs/lab01/lab01.md)