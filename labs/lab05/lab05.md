# Lab 05 - Movies

![lablevel](https://img.shields.io/badge/Lab%20Difficulty-Very%20Hard-red)

There are **no** detailed instructions for this lab.  Load the data from the data folder, import it into a graph and run some queries.

## Steps

1.  Copy all the files from the `data` directory into your Lakehouse `Files` area
2.  Use the `Load to tables` process for each file.  The files are parquet format.
- Create them as new tables
3.  Inspect the loaded files in the Lakehouse
4.  Create a graph ...
- Add nodes director, film, actor
- Add edges directed, appearedIn

## Example

![chris](/labs/lab05/images/chris-nolan.png)

## Example queries

```gql
MATCH (node_Director:`Director`)-[edge1_directed:`directed`]->(node_Films:`Films`),
      (node_Actor:`Actor`)-[edge2_appearedIn:`appearedIn`]->(node_Films:`Films`)
WHERE node_Director.`directorName` = "Rob Reiner"
RETURN TO_JSON_STRING(node_Director) AS `Director`,
       TO_JSON_STRING(edge1_directed) AS `edge_1_directed`,
       TO_JSON_STRING(node_Actor) AS `Actor`,
       TO_JSON_STRING(edge2_appearedIn) AS `edge_2_appearedIn`,
       TO_JSON_STRING(node_Films) AS `Films`
LIMIT 1000
```

```gql
-- Films where Brad and Angelina appeared together; clean
MATCH (a1:actor)-[e1:appearedIn]->(f:film)<-[e2:appearedIn]-(a2:actor)
WHERE a1.actorName = "Brad Pitt"
  AND a2.actorName = "Angelina Jolie"
RETURN TO_JSON_STRING(a1) AS actor1,
       TO_JSON_STRING(a2) AS actor2,
       TO_JSON_STRING(e1) AS edge1,
       TO_JSON_STRING(e2) AS edge2,
       TO_JSON_STRING(f) AS film
LIMIT 1000
```

## Next Steps
- [Home](/README.md)