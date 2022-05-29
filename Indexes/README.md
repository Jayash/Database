# Index

- Sequential Scan: The Seq Scan operation scans the entire relation (table) as stored on disk (like TABLE ACCESS FULL)
- Parallel Sequential Scan: when multiple worker does sequential scan
- Index Scan: The Index Scan performs a B-tree traversal, walks through the leaf nodes to find all matching entries, and fetches the corresponding table data.
- Index only scan: when only select the indexed column it doesn't have to go to heap to fetch the rows

A Bitmap Heap Scan is the most common parent node of a Bitmap Index Scan, but a plan may also combine several different Bitmap Index Scans with BitmapAnd or BitmapOr nodes before actually fetching the underlying data. This allows Postgres to use two different indexes at once to execute a query.

Indexes are stored persistent storage 

In composite index if only right side column is checked then query optimizer will do a sequential scan instead of index scan
<img src="https://user-images.githubusercontent.com/7610065/170886732-f2c8aa8f-5c15-4f36-8265-3d0c9ecfc740.png" width="500" height="250">

