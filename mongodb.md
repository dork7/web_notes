# MongoDB

MongoDB uses key-value storage in the collection of documents

# MongoDB Sharding
- Sharding is a method for distributing a single dataset across multiple databases
- Sharding is a method of splitting and storing a single logical dataset in multiple databases
- It is the process of writing data across different servers to distribute the read and write load and data storage requirements.

## Why Sharding?
- Database systems having big data sets or high throughput requests can doubt the ability of a single server.
- For example, High query flows can drain the CPU limit of the server.
- The working set sizes are larger than the system’s RAM to stress the I/O capacity of the disk drive.


Advantages of Sharding : 

Sharding adds more server to a data field automatically adjust data loads across various servers.
The number of operations each shard manage got reduced.
It also increases the write capacity by splitting the write load over multiple instances.
It gives high availability due to the deployment of replica servers for shard and config.
Total capacity will get increased by adding multiple shards.

____
# MongoDB Replication
Replication is the method of duplication of data across multiple servers.
- Replica sets are the clusters of N different nodes that maintain the same copy of the data set.
- The primary server receives all write operations and record all the changes to the data i.e, oplog.
- The secondary members then copy and apply these changes in an asynchronous process.
- All the secondary nodes are connected with the primary nodes. there is one heartbeat signal from the primary nodes. If the primary server goes down an eligible secondary will hold the new primary.

## Why Replication?
- High Availability of data disasters recovery
- No downtime for maintenance ( like backups index rebuilds and compaction)
- Read Scaling (Extra copies to read from)

___
## Replica sets
- A replica set in MongoDB is a group of mongod processes that maintain the same data set
- The set of servers that maintain the same copy of data is known as replica servers or MongoDB instances.

## Clusters
- A cluster distributes the workload and stores pieces of data (shards) across multiple servers