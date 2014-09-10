shareddictlogdb: Low-overhead database(eg no SQLite-style index copying) with index support.
===============
* Log-structured db for row storage optimized for fast appends
* shared-dictionary(eg store the shared dictionary alongside the data) compression and/or columnar compression
* Low index overhead: indexes should either use short hashes(compare actual data in case of collisions) or point back at original data for long strings
* no fsync during normal operation, support log replication for redundancy instead
