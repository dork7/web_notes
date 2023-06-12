# MongoDB

MongoDB uses key-value storage in the collection of documents

# MongoDB Sharding

- Sharding is a method for allocating data across multiple machines. 
- It is the process of writing data across different servers to distribute the read and write load and data storage requirements.
- By sharding, you divided your collection into different parts.

## Why Sharding?
- Database systems having big data sets or high throughput requests can doubt the ability of a single server.
- For example, High query flows can drain the CPU limit of the server.
- The working set sizes are larger than the system’s RAM to stress the I/O capacity of the disk drive.

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

## Replica servers
The set of servers that maintain the same copy of data is known as replica servers or MongoDB instances.