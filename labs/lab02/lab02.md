# Lab 02 - Weighted Graph

![lablevel](https://img.shields.io/badge/Lab%20Difficulty-Easy-green)

![Weighted Graph](/labs/lab02/images/Weighted_network.png)

This lab will create a simple graph based on weighted graph example from the Wikipedia page [Graph](https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)).  It will work with the tables `nod_letters` and `edg_letters` which were created by the initial notebook.  There will be fewer screenshots in this lab as the first lab should have established the principles.

> [!IMPORTANT]  
> Make sure you have run some SQL queries against the tables first.

## Steps

1. Create a new graph item  
- From the home page of your workspace, click **+ New item**  

> [!TIP]
> Enter `graph` in the filter box to filter items

- Select `Graph model (preview)`
- Name it `grphWeighted` and click **Create**

> [!TIP]
> For those of you who don't believe in being able to effectively troubleshoot problems at 3am, please feel free to leave the item type prefix **off**.




2. Add data to the graph
- Click the **Get data** button
- Select the Lakehouse from the workspace created earlier

-  Double-click your Lakehouse or click the **Connect** button on the lower right-hand side

- A list of tables should appear
- Select `nod_letters` and `edg_letters`
- Click **Load**
- The two tables should appear on the right in the **Data** section

3. Add Nodes to the graph
- Click **Add node**
- Configure the node as follows:

| Property      | Value         |
|---------------|---------------|
| Label         | Letters       |
| Mapping Table | nod_letters   |
| Id            | letters        |

The configuration should look like this:

![Node Config](/labs/lab02/images/node-config.png)

- Click **Confirm**

4. Add Edges to the graph
- Click **Add edge**
- Configure the edge as follows:

| Property                  | Value         |
|---------------------------|---------------|
| Label                     | relatesTo     |
| Mapping Table             | edg_letters   |
| Source Node               | Letters       |
| Mapping table column from | fromLetter    |
| Target Node               | Letters       |
| Mapping table column to   | toLetter      |

![Edge Config](/labs/lab02/images/edge-config.png)


5.  Add **weight** to the graph via the Properties menu
 - Click on **Model** in the **Modes** section on the left-hand side
 - Double-click on the relationship `relatesTo`
 - Click on **Properties** and add in `weight` as an `integer`

![Add weight](/labs/lab02/images/add-weight.png)


- Click **Save**.  This may take some time.  Allow several minutes.

- When the Load banner disappears, the graph data should be loaded

6. Render the graph
- Click on **Query**
- Add the *Nodes* and *Edges* from the menu on the right-hand side.

- Press **Run query**

7. Arrange the graph
- After running the query, show the weight property on the edge `relatesTo`

![Weighted Graph](/labs/lab02/images/weighted-graph.png)

- Observe the `weights` property on the relationship

> [!TIP]
> Yes the waits on loading relatively small volumes of data into graph can become frustrating while the product is in preview!

## Exercises
The exercises do **not** contain step by step instructions.  Work with the existing lab instructions, your colleagues and the instructor to complete them.

### Exercise 2.1
- Make sure you can see the weight on the edge.  If you can't add it, you might have missed a step.
- Go back to the graph model and fix it up

> [!TIP]
> Create a new graph item with updated data rather than attempting to update your existing item

<details>
<summary>💡 Hint</summary>
Add weight via the Properties menu in the Model view
</details>

### Exercise 2.2
- Click **Query Builder** > **Code Editor**.  What do you see?

## Questions
- How is this graph different to the first one?
- When would you use weighted vs unweighted graphs?

## Next Steps
- [Lab 03 - Social Network](/labs/lab03/lab03.md)
- [Home](/README.md)