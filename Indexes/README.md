# Index

- Sequential Scan: The Seq Scan operation scans the entire relation (table) as stored on disk (like TABLE ACCESS FULL)
- Parallel Sequential Scan: when multiple worker does sequential scan
- Index Scan: The Index Scan performs a B-tree traversal, walks through the leaf nodes to find all matching entries, and fetches the corresponding table data.
- Index only scan: when only select the indexed column it doesn't have to go to heap to fetch the rows

A Bitmap Heap Scan is the most common parent node of a Bitmap Index Scan, but a plan may also combine several different Bitmap Index Scans with BitmapAnd or BitmapOr nodes before actually fetching the underlying data. This allows Postgres to use two different indexes at once to execute a query.

## Index Storage
Indexes are stored in RAM and if it becomes to large it gets stored in persistent storage

## Cluster Index
A clustered index is an index which defines the physical order in which table records are stored in a database. Since there can be only one way in which records are physically stored in a database table, there can be only one clustered index per table. By default a clustered index is created on a primary key column.

The secondary index is an indirect way to access the data. Unlike the primary (clustered) index, when you traverse the secondary index in InnoDB and you reach the leaf node you find a primary key value for the corresponding row the query is looking for. Using this value you traverse the primary index to fetch the row. This means 2 index look ups in InnoDB.
For MyISAM because the leaf of the secondary node is a pointer to the actual row you only require 1 index lookup.


In composite index if only right side column is checked then query optimizer will do a sequential scan instead of index scan
<img src="https://user-images.githubusercontent.com/7610065/170886732-f2c8aa8f-5c15-4f36-8265-3d0c9ecfc740.png" width="500" height="250">

## Bloom Filters

A Bloom filter is a space-efficient probabilistic data structure, conceived by Burton Howard Bloom in 1970, that is used to test whether an element is a member of a set. For example, checking availability of username is set membership problem, where the set is the list of all registered username. The price we pay for efficiency is that it is probabilistic in nature that means, there might be some False Positive results. False positive means, it might tell that given username is already taken but actually it’s not.

https://www.geeksforgeeks.org/bloom-filters-introduction-and-python-implementation/

## Working with a Billion-Row Table

1. Sharding
2. partitioning
3. indexing 

