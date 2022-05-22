# ACID

## Transaction

<img src="https://user-images.githubusercontent.com/7610065/169667163-757de309-7959-4e21-85d4-0158bd574c41.png" width="500" height="250">

<img src="https://user-images.githubusercontent.com/7610065/169667206-6fe48e00-f924-4da0-9ce1-226fee7d6fa7.png" width="500" height="250">

## Atomicity

<img src="https://user-images.githubusercontent.com/7610065/169667467-83e78beb-4894-4647-b720-6c79e232f244.png" width="500" height="250">

## Isolation

<img src="https://user-images.githubusercontent.com/7610065/169667467-83e78beb-4894-4647-b720-6c79e232f244.png" width="500" height="250">

### Dirty Read

Read data while it is still updating, in case transaction might rollback.

<img src="https://user-images.githubusercontent.com/7610065/169685097-c91c2c21-5e49-4326-8908-eaabc2492162.png" width="500" height="250">

### Non-repeatable Read

two read for same row might result in different data, it might happen when another transaction update the row and commits it.

<img src="https://user-images.githubusercontent.com/7610065/169685298-486ebc55-6cbd-4b02-8104-165d173d17e9.png" width="500" height="250">
