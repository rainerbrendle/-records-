# {records}
Final {records} architecture specification for a Active Database Cluster.

(c) 2023 Rainer Brendle, Port Charlotte, FL, USA

## Basic Assumption
Every transaction goes from collecting input operations, which the form a logical message, when completed. A message describes a wish of intention for a record to be created.
The record is send to a distributed and shared database cluster, which is organized and distributed around a purpose. The purpose describes what in computer science once was called an "Actor". It is logically a "class", but not in the Java object oriented sense. More int he sense of SQL or Cott's theorem on first-order logic.  It is about a message recipient, which is about recording results in a organized manner and then can create "matriealied views" on this. 

Results are recorded as journals of received messages. Journals form time series of collected notification in the end. Since these "time series" are stable, immutable records, we can also thransform them in - in the end - arbitrary projections.

Both the creation of the message and the sending an receiving of the immutable message as a record are Rest services and can be represent as Rest related services, but hey are similiar, but not the same.  

### Prior Art
May be a good collection on prior art may be found in Pat Helland's CIDR Paper of 2015.

https://www.cidrdb.org/cidr2015/Papers/CIDR15_Paper16.pdf

which contains a quite resonable collection of older work.

We have two implmentations - one is done in Go and another one in Python. Both make the simple assumption that both editing  messages and storing and managing immutable messages as records are REST services, which are similiar but different. The implmentation can be don on PostgreSQL using Docker Containers. We are suing Closures either in Go or in Python to manage similarity and to configura various services.
