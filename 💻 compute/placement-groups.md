### Strategy
* Cluster
  - Instances are placed in single Availability Zone
  - Provides low latency, high throughput
  - Available only on certain instance types
  - Works best with instances that support enhanced networking
* Partition
  - Ensures that each partition within a placement group has its own set of racks
  - No two partitions within a placement group share the same racks, allowing you to isolate the impact of hardware failure within your application
  - The instances in a partition do not share racks with the instances in the other partitions
  - Used to deploy large distributed and replicated workloads, such as HDFS, HBase, and Cassandra, across distinct racks
* Spread
  - Instances are placed on distinct hardware
  - Recommended for applications that have a small number of critical instances that should be kept separate from each other
  - Spread level placement groups provide access to distinct hardware, and are therefore suitable for mixing instance types or launching instances over time
