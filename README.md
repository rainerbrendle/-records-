# {records}
Final {records} architecture specification for the creation of an Active Database Cluster of immutable records.

(c) 2023 Rainer Brendle, Port Charlotte, FL, USA

## Basic Assumption
Every more complex transactions, which go beyond simple Wordpress-like applications, go from collecting input operations defining an intention as a form of a logical message, when completed. A copleted message describes a wish of intention for a record to be created.

Many applications follow this pattern - going from intention to final immutable records. 

Records are asynchronous messages, which are send to a distributed and shared database cluster, which is organized and distributed around purposes. Often this can mean a workplace or an account or both. 

The recipient assigned to a message describes what in computer science once was called an "Actor" at MIT years ago. It is logically a "class", but not in the Java object-oriented sense. More in the sense of SQL or better in the sense of Cott's theorem about first-order logic.  

An Actor is a message resipient, which is about recording results in a organized and timely ordered manner and then is to create "materialized views" on this as logical projections. Ypu never delete records, records are descriptions of the past. 

Results are recorded as timely ordered journals of received messages on an "Actor". Journals form a time series of collected notification in the end on a topic. Since these "time series" are stable and immutable records, we can also thransform them into - in the end - arbitrary projections. 

Both the creation of the message and the sending an receiving of the immutable message as a record form Rest services and can be represented as Rest related services, but hey are similiar, but not the same.  

### Prior Art
May be a good collection on prior art on distributed computing may be found in Pat Helland's CIDR Paper of 2015.

https://www.cidrdb.org/cidr2015/Papers/CIDR15_Paper16.pdf

which contains a quite resonable collection of older work from various people.

We have two implmentations - one is done in Go and another one in Python. Both make the simple assumption that both editing messages, publishing a message and storing and managing immutable messages as records are REST services, which are similiar services, but different simply becasue the intention is about the future, while records are about the past.  

The implmentation can be done on PostgreSQL using Docker Containers. We are suing Closures either in Go or in Python to manage similarity and to configure various services. All is purely functionsl programming and can be seen as a low-code platform, if we want to.

The Golang version is in a separate git repository as well as the Python version.
Go has the benefit that it is a strong-typed language and we can switch between strong-typed modules and loose-coupling between them, such that we can have a mostly schema-free database implementation, while persistent messages are either JSON or AVRO messages. 

The Golang version is using Closures on anonymous REST functions on PosttgreSQL bases ahsrded database instances and the introspection capabilities of GO to map JSON data to GO models and vice versa. Also it uses the asynchronous communication capabilities of Go using channels.

