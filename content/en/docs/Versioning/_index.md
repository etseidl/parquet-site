---
title: "Format Versioning"
linkTitle: "Format Versioning"
weight: 8
description: >
  Documentation about versions of the Parquet File Format.
---


The two major versions of Parquet are refered to as `V1` and `V2`. Saying that a given
file is `V1` generally implies it uses only features that were present in the `1.0.0`
version of the Parquet format specification (`parqet-format v1.0.0`). Saying that a file
is `V2`, however, is not as clearly defined. Instead, one should refer to the version of
the Parquet format specification that will include add features present in the file.

The following sections define those features that can be used to version a file. A feature
matrix is also included aid users in picking compatible versions of various Parquet
implementations to improve compatibility.

V1 baseline capabilities

V2 timeline of added capabilities