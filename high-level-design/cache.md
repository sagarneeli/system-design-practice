Caches take advantage of the locality of reference principle: recently requested data is likely to be requested again. They are used in almost every computing layer: hardware, operating systems, web browsers, web applications, and more. A cache is like short-term memory: it has a limited amount of space, but is typically faster than the original data source and contains the most recently accessed items. Caches can exist at all levels in architecture, but are often found at the level nearest to the front end, where they are implemented to return data quickly without taxing downstream levels.

 if your load balancer randomly distributes requests across the nodes, the same request will go to different nodes, thus increasing cache misses. Two choices for overcoming this hurdle are global caches and distributed caches.

 CDNs are a kind of cache that comes into play for sites serving large amounts of static media. In a typical CDN setup, a request will first ask the CDN for a piece of static media; the CDN will serve that content if it has it locally available. If it isn’t available, the CDN will query the back-end servers for the file, cache it locally, and serve it to the requesting user.

 Cache Invalidation
 Write-through cache: Under this scheme, data is written into the cache and the corresponding database simultaneously.

 Write-around cache: This technique is similar to write-through cache, but data is written directly to permanent storage, bypassing the cache.

 Write-back cache: Under this scheme, data is written to cache alone, and completion is immediately confirmed to the client. The write to the permanent storage is done after specified intervals or under certain conditions. This results in low-latency and high-throughput for write-intensive applications; however, this speed comes with the risk of data loss in case of a crash or other adverse event because the only copy of the written data is in the cache

 Cache eviction policies#
Following are some of the most common cache eviction policies:

First In First Out (FIFO): The cache evicts the first block accessed first without any regard to how often or how many times it was accessed before.
Last In First Out (LIFO): The cache evicts the block accessed most recently first without any regard to how often or how many times it was accessed before.
Least Recently Used (LRU): Discards the least recently used items first.
Most Recently Used (MRU): Discards, in contrast to LRU, the most recently used items first.
Least Frequently Used (LFU): Counts how often an item is needed. Those that are used least often are discarded first.
Random Replacement (RR): Randomly selects a candidate item and discards it to make space when necessary.

Data partitioning is a technique to break a big database (DB) into many smaller parts. It is the process of splitting up a DB/table across multiple machines to improve the manageability, performance, availability, and load balancing of an application.

Horizontal Partitioning: In this scheme, we put different rows into different tables.
Horizontal Partitioning is also known as Data Sharding.

Vertical Partitioning: In this scheme, we divide our data to store tables related to a specific feature in their own server.

Directory-Based Partitioning: A loosely coupled approach to work around issues mentioned in the above schemes is to create a lookup service that knows your current partitioning scheme and abstracts it away from the DB access code


Simply saying, an index is a data structure that can be perceived as a table of contents that points us to the location where actual data lives. So when we create an index on a column of a table, we store that column and a pointer to the whole row in the index

An index can dramatically speed up data retrieval but may itself be large due to the additional keys, which slow down data insertion & update


A proxy server is an intermediate piece of software or hardware that sits between the client and the server

forward proxies are used to cache data, filter requests, log requests, or transform requests (by adding/removing headers, encrypting/decrypting, or compressing a resource

A forward proxy can hide the identity of the client from the server by sending requests on behalf of the client.

A reverse proxy retrieves resources from one or more servers on behalf of a client. These resources are then returned to the client, appearing as if they originated from the proxy server itself, thus anonymizing the server.

Contrary to the forward proxy, which hides the client’s identity, a reverse proxy hides the server’s identity.


Redundancy is the duplication of critical components or functions of a system with the intention of increasing the reliability of the system, usually in the form of a backup or fail-safe, or to improve actual system performance

Replication means sharing information to ensure consistency between redundant resources, such as software or hardware components, to improve reliability, fault-tolerance, or accessibility.

Relational databases are structured and have predefined schemas like phone books that store phone numbers and addresses. Non-relational databases are unstructured, distributed, and have a dynamic schema like file folders that hold everything from a person’s address and phone number to their Facebook ‘likes’ and online shopping preferences.

Relational databases store data in rows and columns. Each row contains all the information about one entity and each column contains all the separate data points.

CAP theorem states that it is impossible for a distributed system to simultaneously provide all three of the following desirable properties:

Consistency (C): All nodes see the same data at the same time. This means users can read or write from/to any node in the system and will receive the same data. It is equivalent to having a single up-to-date copy of the data.

Availability (A): Availability means every request received by a non-failing node in the system must result in a response. Even when severe network failures occur, every request must terminate. In simple terms, availability refers to a system’s ability to remain accessible even if one or more nodes in the system go down.

Partition tolerance (P): A partition is a communication break (or a network failure) between any two nodes in the system, i.e, both nodes are up but cannot communicate with each other. A partition-tolerant system continues to operate even if there are partitions in the system. Such a system can sustain any network failure that does not result in the failure of the entire network. Data is sufficiently replicated across combinations of nodes and networks to keep the system up through intermittent outages.

In system design, we are doing nothing but
1. Move Data
2. Store Data
3. Transform Data

Availability - Uptime / (Uptime / downtime) -> percentage

99, 99.9, 99.99, 99.999 %

1 year
Eg 3.65 days for 99 availability
    5 mins for 99.999 availability

Reliability -> Probability system won't fail Eg add more servers 

SLO -> Eg Availability - 99.999 % ~ 5 mins
SLA - SLO + Extra -> Refund money

DOS - Denial of Service attack
DDOS - Distribute DOS

Vertical Scaling - Increases availability
Horizontal Scaling - Increases reliability

Fault Tolerance - System can tolerate faulty behaviour - Eg disaster. In directly related to reliability
Redundancy - We duplicate data across different servers

Throuhgput = amount of something or operations / over a period of time
How many requests / seconds can our server handle => Client to server
queries / second => server to DB
How much data can the system handle - bytes / second => Pipelining data


