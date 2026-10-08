# Appendix B. Geo-replication

*Geo-replication* is a common mechanism used to provide disaster recovery in multi-datacenter deployments. Unlike other pub-sub messaging systems that require additional processes to mirror messages between data centers, geo-replication is automatically performed by Pulsar brokers and can be enabled, disabled, or dynamically changed at runtime. Traditional geo-replication mechanisms typically fall into one of two categories: synchronous or asynchronous. Apache Pulsar comes with multi-datacenter replication as an integrated feature that supports both of these geo-replication strategies. In the following examples, I will assume that we are deploying our Pulsar instance across the three cloud provider regions: US-West, US-Central, and US-East.


## 子目录

- [B.1 Synchronous geo-replication](<appendix-b.-geo-replication/b.1-synchronous-geo-replication.md>)
- [B.2 Asynchronous geo-replication](<appendix-b.-geo-replication/b.2-asynchronous-geo-replication.md>)
- [B.3 Asynchronous geo-replication patterns](<appendix-b.-geo-replication/b.3-asynchronous-geo-replication-patterns.md>)
