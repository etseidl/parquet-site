---
title: "Baseline V1 Features"
linkTitle: "Baseline V1 Features"
weight: 1
---

physical types:
  BOOLEAN
  INT32
  INT64
  INT96
  FLOAT
  DOUBLE
  BYTE_ARRAY
  FIXED_LEN_BYTE_ARRAY

converted types:
  UTF8
  MAP
  MAP_KEY_VALUE
  LIST

encodings:
  PLAIN
  PLAIN_DICTIONARY
  RLE
  BIT_PACKED

compression codecs:
  UNCOMPRESSED
  SNAPPY
  GZIP
  LZO

page types:
  DATA_PAGE
  INDEX_PAGE
  DICTIONARY_PAGE

data_page:
  num_values
  encoding
  definition_level_encoding
  repetition_level_encoding

dictionary_page:
  num_values
  encoding

column_meta_data:
  type
  encodings
  path_in_schema
  codec
  num_values
  total_uncompressed_size
  total_compressed_size
  key_value_metadata
  data_page_offset
  index_page_offset
  dictionary_page_offset

column_chunk:
  file_path
  file_offset
  meta_data

row_group:
  columns
  total_byte_size
  num_rows

file_meta_data:
  version
  schema
  num_rows
  row_groups
  key_value_metadata
  created_by