# KAFKA

## Producer
- Produce a message ( frontend, application)
- Producer produce a message and send it to a topic from where consumer can read


## Consumer
- Consume a message ( store in db, perform action on message)

## Topic
- Logical partitioning of the messages ( orderTopic, deliveryTopic,  )
- Partition of messages based on subjects

## Partitions
- Partition inside a topic
- Dividing a single topic into multiple partitions
- Data set is divided into chunks

### Example
> - Earth location data can be stored inside location **topic**, so we can partition data based on area.


~~~
# IMPORTANT
-> One consumer can consume multiple partition
-> One partition can be consumed by only one consumer
~~~


