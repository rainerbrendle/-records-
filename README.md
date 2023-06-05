# {records}
Final {records} architecture specification.

## Basic Assuption
Every transaction goes from collecting input operations, which form a logical message. A message describes a wish of intention for a record to be created.
The record is send to a distributed and shared database cluster, which is organized and distributed around a purpose. The purpose describes what in computer science once was called an "Actor". It is logically a "class", but not in the Java object oriented sense. More int he sense of SQL or Cott's theore on first-order logic.  It is a message recipient, which is about recording results in a organized manner.

Results are recorded as journals and from journals, which are time series in the end. Since these "time series" are stable, immutable records, we can also thransform them in - in the end - arbitrary projections.
