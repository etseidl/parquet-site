---
title: "Metadata"
linkTitle: "Metadata"
weight: 5
---
There are two types of metadata: file metadata, and page header metadata.
In the diagram below, file metadata is described by the `FileMetaData`
structure. This file metadata provides offset and size information useful
when navigating the Parquet file. Page header metadata (`PageHeader` and
children in the diagram) is stored in-line with the page data, and is
used in the reading and decoding of said data.


All thrift structures are serialized using the TCompactProtocol. The full
definition of these structures is given in the Parquet
[Thrift definition](https://github.com/apache/parquet-format/blob/master/src/main/thrift/parquet.thrift).


![File Layout](/images/FileFormat.gif)
