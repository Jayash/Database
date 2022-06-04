# Database

## ACID
## Database Internal
## Indexes

- DDL Commands:	CREATE, DROP, RENAME
- DML Commands: ALTER.	INSERT, UPDATE and DELETE.

## Problems in Long Running Transactions

- connection reset/close/timeout (if user goes to the bathroom)
- database configuration (database are mostly pre-configured for many short transactions, not long ones. E.g. the undo log that keeps track of what has been done during the tx may need to be tuned)
- lock issues, even maybe deadlocks (the longer the transactions are, bigger the chances are the same lock is acquired twice possibly in conflicting order)
