# Index

- Sequential Scan
- Parallel Sequential Scan: when multiple worker does sequential scan
- Index Scan:
- Index only scan: when only select the indexed column

Indexes are stored persistent storage 

In composite index if only right side column is checked then query optimizer will do a sequential scan instead of index scan
<img src="https://user-images.githubusercontent.com/7610065/170886732-f2c8aa8f-5c15-4f36-8265-3d0c9ecfc740.png" width="500" height="250">

