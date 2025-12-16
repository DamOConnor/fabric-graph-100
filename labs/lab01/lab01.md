# Lab 01 - Numbers

![Graph 1 to 6](/labs/lab01/images/graph-1-6.png)

This lab will create a simple graph based on the Wikipedia page [Graph](https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)).  It will work with the tables `nod_numbers` and `edg_numbers` which were created by the initial notebook.

## Steps

1. Create a new graph item  
- From the home page of your workspace, click **+ New item**  

> [!TIP]
> Enter `graph` in the filter box to filter items

- Select `Graph model (preview)`
- Name it `grp1to6`

![Create Graph Model](/labs/lab01/images/create-graph-model.png)

2. Add data to the graph
- Click the **Get data** button
- Select the Lakehouse from the workspace created earlier
![image](/labs/lab01/images/select-lakehouse.png)

-  Double-click your Lakehouse or click the **Connect** button on the lower right-hand side

- A list of tables should appear
- Select `nod_numbers` and `edg_numbers`

3. Add Nodes to the graph
- Click **Add node**
  nod edges

4. Add Edges to the graph
!!TODO

5. Render the graph
6. Decorate the graph

After running the query ...
7.  Arrange your graph in the same manner as the image above.

> [!TIP]
> Generally speaking, rearrange the graph is a waste of time as the layout is not saved.  However it will be useful for this exercise.

## Exercises
The exercises do **not** contain step by step instructions.  Work with the existing lab instructions, your colleagues and the instructor to complete them.

### Exercise 1.1
- You should see one of the relationships is missing.  Which one?
- Go back to the notebook and fix it up

> [!TIP]
> Recreate your graph item rather than attempt to attempting to update it

<details>
<summary>💡 Hint</summary>
Go back to the notebook if you are stuck. Check the edge table for missing relationships.
</details>

## Questions
- Why graph?
- What is the difference between the graph in the image and the graph you have created?
- It is possible to create the graph *without* using separate node and edge tables:
  - why would you use this approach?
  - why would you **not** use this approach?
- Attempt to model the data this way (all one table) and build a graph from it if you have time to waste

> [!TIP]
> Move on to the next lab.  It's more interesting that attempting to remodel the data.

## Next Steps
- [Lab 02 - Weighted Graph](/labs/lab02/lab02.md)
- [Home](/README.md)


