---
title: "V2 Features by Version"
linkTitle: "V2 Features by Version"
weight: 2
---

The features listed here are additions since V1 (in baseline doc).

2.0.0
converted types:
  ENUM converted

encodings:
  deprecated BIT_PACKED
  DELTA_BINARY_PACKED
  DELTA_LENGTH_BYTE_ARRAY
  DELTA_BYTE_ARRAY
  RLE_DICTIONARY

page types:
  DATA_PAGE_V2

data_page_v2:
  num_values
  num_nulls
  num_rows
  encoding
  definition_levels_byte_length
  repetition_levels_byte_length
  is_compressed
  statistics

dictionary_page:
  is_sorted

column_meta_data:
  statistics

row_group:
  sorting_columns

2.1.0
adds notion of logical types UTF8 and DECIMAL, but still implemented as converted type

converted types:
  DECIMAL

data_page:
  statistics

schema_element:
  scale
  precision

2.2.0
move to apache

converted types:
  INT_8
  INT_16
  INT_32
  INT_64
  UINT_8
  UINT_16
  UINT_32
  UINT_64
  DATE
  TIME_MILLIS
  TIMESTAMP_MILLIS
  INTERVAL
  JSON
  BSON

schema_element:
  field_id

column_meta_data:
  encoding_stats

2.3.0
no changes

2.3.1
converted types:
  TIME_MICROS
  TIMESTAMP_MICROS

adds formal definition of logical LIST and MAP

2.4.0
cleaned up ordering of types, adds column_orders field, adds page indexes

statistics:
  deprecate min and max
  max_value
  min_value

logical types:
  converted type is deprecated, new logical type structure added to schema
  STRING
  MAP
  LIST
  ENUM
  DECIMAL
  DATE
  TIME
  TIMESTAMP
  INTEGER
  UNKNOWN
  JSON
  BSON

schema_element:
  logicalType

compression:
  BROTLI
  LZ4
  ZSTD

column_chunk
  offset_index_offset
  offset_index_length
  column_index_offset
  column_index_length

file_meta_data:
  column_orders

2.5.0
deprecates INT96 physical type
deprecates use of PLAIN_DICTIONARY enum value for 2.0, prefer RLE_DICTIONARY/PLAIN

2.6.0
logical types:
  UUID
  add NANOS to TimeUnit

2.7.0
adds bloom filters and encryption

column_meta_data:
  bloom_filter_offset

column_chunk:
  crypto_metadata
  encrypted_column_metadata

row_group:
  file_offset
  total_compressed_size
  ordinal

file_meta_data:
  encryption_algorithm
  footer_signing_key_metadata

2.8.0
encodings:
  BYTE_STREAM_SPLIT (for FLOAT and DOUBLE)

2.9.0
converted type officially deprecated

codec:
  LZ4_RAW

2.10.0
adds page/chunk size statistics and histograms

logical types:
  FLOAT16

statistics:
  is_max_value_exact
  is_min_value_exact

column_meta_data:
  bloom_filter_length
  size_statistics

column_index:
  repetition_level_histograms
  definition_level_histograms

offset_index:
  unencoded_byte_array_data_bytes