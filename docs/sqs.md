# Amazon SQS (Simple Queue Service)

## intro

- simple messaging queue, sends data to one consumer at a time.
- can have a lambda listening on the queue.

## types of queue

### standard queues

- support a nearly unlimited number of transactions per second per API action.
- messages are delivered at least once, but sometimes more than once.
- messages are usually dielivered in order but sometime get out of order.

### FIFO queues

- First In First Out
- up to 300 messages per second
- guaranteed ordering
- messages delevered exactly once - no duplicates

## pricing

- first million each month requests are free.
- after this, pay per request and also possible by volume of data.
