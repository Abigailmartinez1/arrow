<!---
  Licensed to the Apache Software Foundation (ASF) under one
  or more contributor license agreements.  See the NOTICE file
  distributed with this work for additional information
  regarding copyright ownership.  The ASF licenses this file
  to you under the Apache License, Version 2.0 (the
  "License"); you may not use this file except in compliance
  with the License.  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing,
  software distributed under the License is distributed on an
  "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
  KIND, either express or implied.  See the License for the
  specific language governing permissions and limitations
  under the License.
-->

# Apache Arrow

[![Fuzzing Status](https://oss-fuzz-build-logs.storage.googleapis.com/badges/arrow.svg)](https://bugs.chromium.org/p/oss-fuzz/issues/list?sort=-opened&can=1&q=proj:arrow)
[![License](http://img.shields.io/:license-Apache%202-blue.svg)](https://github.com/apache/arrow/blob/master/LICENSE.txt)
[![Twitter Follow](https://img.shields.io/twitter/follow/apachearrow.svg?style=social&label=Follow)](https://twitter.com/apachearrow)

## Powering In-Memory Analytics

Apache Arrow is a development platform for in-memory analytics. It contains a
set of technologies that enable big data systems to process and move data fast.

## Usage

The reason for this development platform is to allow users to easily access technologies that process data within large data systems quickly and efficiently.  The goal of this platform is for in-memory analytics to move data fast. Apache Arrow utilizes an in-memory format that allows users to store various data types while allowing communication between processes and environments by using the IPC format. The Arrow flight RPC protocol is based on the IPC format which allows remote services to exchange Arrow data with application-defined semantics. 

With versatile access to numerous data types, the Arrow libraries allow for table-like containers. The fast metadata messaging layer is suitable for processing information from large data systems such as databases and storage servers. The self-describing binary format allows users to use remote procedure calls and interprocess communication. Large data systems are not effectively compatible with traditional data processing application software due to the numerous fields and attributes. The Arrow libraries support flat or nested data types which are imperative for conversation to and from other data formats. This allows the processing of large amounts of data to have fast and efficient data transport.

## Major Components of The Project

 - [The Arrow Columnar In-Memory Format](https://github.com/apache/arrow/blob/master/docs/source/format/Columnar.rst):
   a standard and efficient in-memory representation of various datatypes, plain or nested
 - [The Arrow IPC Format](https://github.com/apache/arrow/blob/master/docs/source/format/Columnar.rst#serialization-and-interprocess-communication-ipc):
   an efficient serialization of the Arrow format and associated metadata,
   for communication between processes and heterogeneous environments
 - [The Arrow Flight RPC protocol](https://github.com/apache/arrow/tree/master/format/Flight.proto):
   based on the Arrow IPC format, a building block for remote services exchanging
   Arrow data with application-defined semantics (for example a storage server or a database)
 - [C++ libraries](https://github.com/apache/arrow/tree/master/cpp)
 - [C bindings using GLib](https://github.com/apache/arrow/tree/master/c_glib)
 - [C# .NET libraries](https://github.com/apache/arrow/tree/master/csharp)
 - [Gandiva](https://github.com/apache/arrow/tree/master/cpp/src/gandiva):
   an [LLVM](https://llvm.org)-based Arrow expression compiler, part of the C++ codebase
 - [Go libraries](https://github.com/apache/arrow/tree/master/go)
 - [Java libraries](https://github.com/apache/arrow/tree/master/java)
 - [JavaScript libraries](https://github.com/apache/arrow/tree/master/js)
 - [Plasma Object Store](https://github.com/apache/arrow/tree/master/cpp/src/plasma):
   a shared-memory blob store, part of the C++ codebase
 - [Python libraries](https://github.com/apache/arrow/tree/master/python)
 - [R libraries](https://github.com/apache/arrow/tree/master/r)
 - [Ruby libraries](https://github.com/apache/arrow/tree/master/ruby)
 - [Rust libraries](https://github.com/apache/arrow-rs)

Arrow is an [Apache Software Foundation](https://www.apache.org) project. Learn more at
[arrow.apache.org](https://arrow.apache.org).

## What's in the Arrow libraries?

The reference Arrow libraries contain many distinct software components:

- Columnar vector and table-like containers (similar to data frames) supporting
  flat or nested types
- Fast, language agnostic metadata messaging layer (using Google's Flatbuffers
  library)
- Reference-counted off-heap buffer memory management, for zero-copy memory
  sharing and handling memory-mapped files
- IO interfaces to local and remote filesystems
- Self-describing binary wire formats (streaming and batch/file-like) for
  remote procedure calls (RPC) and interprocess communication (IPC)
- Integration tests for verifying binary compatibility between the
  implementations (e.g. sending data from Java to C++)
- Conversions to and from other in-memory data structures
- Readers and writers for various widely-used file formats (such as Parquet, CSV)

## Implementation status

The official Arrow libraries in this repository are in different stages of
implementing the Arrow format and related features.  See our current
[feature matrix](https://github.com/apache/arrow/blob/master/docs/source/status.rst)
on git master.

## How to Contribute

Apache Arrow is not only a development platform for in-memory analytics but an ever-growing community of users and data system developers. To contribute to the project, please read our latest [project contribution guide][5].

## Getting involved

Even if you do not plan to contribute to Apache Arrow itself or Arrow
integrations in other projects, we'd be happy to have you involved:

- Join the mailing list: send an email to
  [dev-subscribe@arrow.apache.org][1]. Share your ideas and use cases for the
  project.
- Follow our activity on [GitHub issues][3]
- [Learn the format][2]
- Contribute code to one of the reference implementations

[1]: mailto:dev-subscribe@arrow.apache.org
[2]: https://github.com/apache/arrow/tree/master/format
[3]: https://github.com/apache/arrow/issues
[4]: https://github.com/apache/arrow
[5]: https://github.com/apache/arrow/blob/master/docs/source/developers/contributing.rst
