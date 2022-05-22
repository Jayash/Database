# ACID

## Transaction

<img src="https://user-images.githubusercontent.com/7610065/169667163-757de309-7959-4e21-85d4-0158bd574c41.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/169667206-6fe48e00-f924-4da0-9ce1-226fee7d6fa7.png" width="500" height="250">

## Atomicity

<img src="https://user-images.githubusercontent.com/7610065/169667467-83e78beb-4894-4647-b720-6c79e232f244.png" width="500" height="250">

## Isolation

- Read Phenomena -> Dirty Read, Non-repeatable Read, Phantom Read, Loat update
- Isolation Levels is invented to fixed read phenomena

<img src="https://user-images.githubusercontent.com/7610065/169667467-83e78beb-4894-4647-b720-6c79e232f244.png" width="500" height="250">

### Dirty Read

A dirty read occurs when a transaction reads data that has not yet been committed.

<img src="https://user-images.githubusercontent.com/7610065/169685097-c91c2c21-5e49-4326-8908-eaabc2492162.png" width="500" height="250">

### Non-repeatable Read

two read for same row might result in different data, it might happen when another transaction update the row and commits it.

<img src="https://user-images.githubusercontent.com/7610065/169685298-486ebc55-6cbd-4b02-8104-165d173d17e9.png" width="500" height="250">

## Phantom Read

A Phantom read occurs when one user is repeating a read operation on the same records, but has new records in the results.

<img src="https://user-images.githubusercontent.com/7610065/169685552-83fa4e09-0d1a-4e8c-b0d6-3af2a6e11472.png" width="500" height="250">

## Lost Update

<img src="https://user-images.githubusercontent.com/7610065/169685651-06fe6223-961f-4c52-a263-04cfd20749f6.png" width="500" height="250">

## Isolation Levels

Snapshot isolation level will not have phantom reads

<img src="https://user-images.githubusercontent.com/7610065/169687922-5af75211-31d3-4ee7-8161-5c49903697a8.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/169687990-49143197-dcac-413a-a5cd-6467490a463a.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/169688201-6bdf8a0d-d7d7-4490-85c0-f647ebccaa58.png" width="500" height="250">




