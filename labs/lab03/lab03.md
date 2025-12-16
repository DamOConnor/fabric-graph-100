# Lab 03 - Social Network

![graphframes tutorial](/labs/lab03/images/graph-frames-tutorial.png)

This lab recreates the social network data
from the [graphframes tutorial](https://github.com/graphframes/graphframes).  It will work with the tables `nod_person` and `edg_follows` which were created by the initial notebook.

> [!IMPORTANT]  
> Make sure you have run some SQL queries against the tables first.

## Steps

1. Create a new graph item  
- From the home page of your workspace, click **+ New item**

> [!TIP]
> Enter `graph` in the filter box to filter items

- Select `Graph model (preview)`
- Name it `grphSocial` and click **Create**


2. Add data to the graph
- Click the **Get data** button
- Select the Lakehouse from the workspace created earlier

-  Double-click your Lakehouse or click the **Connect** button on the lower right-hand side

- A list of tables should appear
- Select `nod_person` and `edg_follows`
- Click **Load**
- The two tables should appear on the right in the **Data** section

3. Add Nodes to the graph
- Click **Add node**
- Configure the node as follows:

| Property      | Value         |
|---------------|---------------|
| Label         | Person        |
| Mapping Table | nod_person    |
| Id            | personId      |

The configuration should look like this:

![Node Config](/labs/lab03/images/node-config.png)

- Click **Confirm**

4. Add Edges to the graph
- Click **Add edge**
- Configure the edge as follows:

| Property                  | Value         |
|---------------------------|---------------|
| Label                     | follows       |
| Mapping Table             | edg_follows   |
| Source Node               | Person        |
| Mapping table column from | src           |
| Target Node               | Person        |
| Mapping table column to   | dst           |

![Edge Config](/labs/lab03/images/edge-config.png)


5.  Add **relationship** to the graph via the Properties menu
 - Click on **Model** in the **Modes** section on the left-hand side
 - Click on the relationship `follows`
 - Click on **Properties** and add in `relationship` as a `string`

![Add relationship](/labs/lab03/images/add-relationship.png)


- Click **Save**.  This may take some time.  Allow several minutes.

- When the Load banner disappears, the graph data should be loaded

6. Render the graph
- Click on **Query**
- Add the *Nodes* and *Edges* from the menu on the right-hand side.

- Press **Run query**

7. Arrange the graph
- After running the query, show the relationship property on the edge `follows`

![Weighted Graph](/labs/lab03/images/alice-bob.png)

- Observe the `relationship` property
- Configure the node to show the `name` property

> [!TIP]
> Yes the waits on loading relatively small volumes of data into graph can become frustrating while the product is in preview!

## Exercises
The exercises do **not** contain step by step instructions.  Work with the existing lab instructions, your colleagues and the instructor to complete them.

### Exercise 3.1
- Make sure you can see the relationship on the edge.  If you can't add it, you might have missed a step.
- Go back to the graph model and fix it up

> [!TIP]
> Create a new graph item with updated data rather than attempting to update your existing item

<details>
<summary>💡 Hint</summary>
Add relationship via the Properties menu in the Model view
</details>

### Exercise 3.2
- Click **Query Builder** > **Code Editor**.  What do you see?

## Questions
- How is this graph different to the first one?
- When would you use weighted vs unweighted graphs?

## Next Steps
- [Lab 04 - Model the room](/labs/lab04/lab04.md)
- [Home](/README.md)