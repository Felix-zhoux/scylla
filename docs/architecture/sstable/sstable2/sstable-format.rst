SSTable format in ScyllaDB
===========================


ScyllaDB supports the same SSTable format as Apache Cassandra 2.1.8, which means
you can simply place SSTables from a Cassandra data directory into a
ScyllaDB data directory—and it will just work

Looking more carefully, you will see that ScyllaDB maintains more,
smaller, SSTables than Cassandra does. On ScyllaDB, each core manages its
own subset of SSTables. This internal sharding allows each core (shard)
to work more efficiently, avoiding the complexity and delays of multiple
cores competing for the same data

.. include:: /rst_include/architecture-index.rst

.. include:: /rst_include/apache-copyrights.rst
