# BTree and B+Tree

<img src="https://user-images.githubusercontent.com/7610065/171045042-87933ca5-25f9-4717-b055-4d44944d5bea.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/171045457-5fbc7b02-75ec-46b3-9ad6-d49d369f1f7f.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/171045538-b143682c-8754-4bb6-9593-2f8203b0a4a1.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/171047119-88ed8ba3-1744-4028-8f2c-8569013eeb7e.png" width="500" height="250">

## Cluster Index
A clustered index is an index which defines the physical order in which table records are stored in a database. Since there can be only one way in which records are physically stored in a database table, there can be only one clustered index per table. By default a clustered index is created on a primary key column.

The secondary index is an indirect way to access the data. Unlike the primary (clustered) index, when you traverse the secondary index in InnoDB and you reach the leaf node you find a primary key value for the corresponding row the query is looking for. Using this value you traverse the primary index to fetch the row. This means 2 index look ups in InnoDB.
For MyISAM because the leaf of the secondary node is a pointer to the actual row you only require 1 index lookup.

<img src="https://user-images.githubusercontent.com/7610065/171256114-a84155ab-7973-404e-a77c-83e526f3cfd1.png" width="500" height="250">



