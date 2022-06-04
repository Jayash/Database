# Database

## ACID
## Database Internal
## Indexes

- DDL Commands:	CREATE Table, DROP, RENAME
- DML Commands: ALTER.	INSERT, UPDATE and DELETE.

## Problems in Long Running Transactions

- connection reset/close/timeout (if user goes to the bathroom)
- database configuration (database are mostly pre-configured for many short transactions, not long ones. E.g. the undo log that keeps track of what has been done during the tx may need to be tuned)
- lock issues, even maybe deadlocks (the longer the transactions are, bigger the chances are the same lock is acquired twice possibly in conflicting order)

## HOT Heap only tuples

To reduce the amount of I/O necessary for UPDATE, the Postgres team added HOT to Postgres. The idea behind HOT is relatively simple. When updating a row, if it is possible, Postgres will place the new copy of the row right next to the old copy of the row. By doing this and marking the old copy row so that Postgres knows the new copy of the row is right next it, Postgres can avoid updating all of the indexes. During an index scan in which the new copy of the row satisfies the filter, Postgres will encounter the old copy of the row. Since the old copy has been specially marked, Postgres will know the new copy is right next to it and can use that instead. This way, Postgres can pretend that all of the indexes point to the new copy of the row, without ever needing to modify the indexes. Currently HOT is only possible when none of the columns being updated are indexed.
