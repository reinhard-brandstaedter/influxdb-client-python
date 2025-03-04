## 1.18.0 [unreleased]

### Features
1. [#237](https://github.com/influxdata/influxdb-client-python/pull/237): Use kwargs to pass query parameters into API list call - useful for the ability to use pagination.
1. [#241](https://github.com/influxdata/influxdb-client-python/pull/241): Add detail error message for not supported type of `Point.field`
1. [#238](https://github.com/influxdata/influxdb-client-python/pull/238): Add possibility to specify default `timezone` for datetimes without `tzinfo`
1. [#262](https://github.com/influxdata/influxdb-client-python/pull/263): Add option `auth_basic` to allow proxied access to InfluxDB 1.8.x compatibility API

### Bug Fixes
1. [#254](https://github.com/influxdata/influxdb-client-python/pull/254): Serialize `numpy` floats into LineProtocol

### Documentation
1. [#255](https://github.com/influxdata/influxdb-client-python/pull/255): Fix invalid description for env var `INFLUXDB_V2_CONNECTION_POOL_MAXSIZE`

## 1.17.0 [2021-04-30]

### Features
1. [#203](https://github.com/influxdata/influxdb-client-python/issues/219): Bind query parameters 
1. [#225](https://github.com/influxdata/influxdb-client-python/pull/225): Exponential random backoff retry strategy 

### Bug Fixes
1. [#222](https://github.com/influxdata/influxdb-client-python/pull/222): Pass configured timeout to HTTP client
1. [#218](https://github.com/influxdata/influxdb-client-python/pull/218): Support for `with .. as ..` statement
1. [#232](https://github.com/influxdata/influxdb-client-python/pull/232): Specify package requirements in `setup.py`
1. [#235](https://github.com/influxdata/influxdb-client-python/pull/235): Write a dictionary-style object without tags

## 1.16.0 [2021-04-01]

### Features
1. [#203](https://github.com/influxdata/influxdb-client-python/pull/203): Configure a client via TOML file
1. [#215](https://github.com/influxdata/influxdb-client-python/pull/215): Configure a connection pool maxsize

### Bug Fixes
1. [#206](https://github.com/influxdata/influxdb-client-python/pull/207): Use default (system) certificates instead of Mozilla's root certificates (certifi.where())
1. [#217](https://github.com/influxdata/influxdb-client-python/pull/217): Fix clone_task function

### API
1. [#209](https://github.com/influxdata/influxdb-client-python/pull/209): Allow setting shard-group durations for buckets via API

### Documentation
1. [#202](https://github.com/influxdata/influxdb-client-python/pull/202): Added an example how to use RxPY and sync batching
1. [#213](https://github.com/influxdata/influxdb-client-python/pull/213): Added an example how to use Buckets API

## 1.15.0 [2021-03-05]

### Bug Fixes
1. [#193](https://github.com/influxdata/influxdb-client-python/pull/193): Fixed `tasks_api` to use proper function to get `Run`

### Documentation
1. [#200](https://github.com/influxdata/influxdb-client-python/pull/200): Updated docs, examples, tests: use `close` instead of `__del__`.

### CI
1. [#199](https://github.com/influxdata/influxdb-client-python/pull/199): Updated stable image to `influxdb:latest` and nightly to `quay.io/influxdb/influxdb:nightly`

## 1.14.0 [2021-01-29]

### Features
1. [#176](https://github.com/influxdata/influxdb-client-python/pull/179): Allow providing proxy option to InfluxDBClient

### CI
1. [#179](https://github.com/influxdata/influxdb-client-python/pull/179): Updated default docker image to v2.0.3

### Bug Fixes
1. [#183](https://github.com/influxdata/influxdb-client-python/pull/183): Fixes to DataFrame writing.
1. [#181](https://github.com/influxdata/influxdb-client-python/pull/181): Encode Point whole numbers without trailing `.0`

### Documentation
1. [#189](https://github.com/influxdata/influxdb-client-python/pull/189): Updated docs about `DeleteApi`.

## 1.13.0 [2020-12-04]

### Features
1. [#171](https://github.com/influxdata/influxdb-client-python/pull/171): CSV parser is able to parse export from UI

### Bug Fixes
1. [#170](https://github.com/influxdata/influxdb-client-python/pull/170): Skip DataFrame rows without data - all fields are nan.

### CI
1. [#175](https://github.com/influxdata/influxdb-client-python/pull/175): Updated default docker image to v2.0.2

## 1.12.0 [2020-10-30]

1. [#163](https://github.com/influxdata/influxdb-client-python/pull/163): Added support for Python 3.9

### Features
1. [#161](https://github.com/influxdata/influxdb-client-python/pull/161): Added logging message for retries

### Bug Fixes
1. [#164](https://github.com/influxdata/influxdb-client-python/pull/164): Excluded tests from packaging

## 1.11.0 [2020-10-02]

### Features
1. [#152](https://github.com/influxdata/influxdb-client-python/pull/152): WriteApi supports generic Iterable type
1. [#158](https://github.com/influxdata/influxdb-client-python/pull/158): Added possibility to specify certificate file path to verify the peer

### API
1. [#151](https://github.com/influxdata/influxdb-client-python/pull/151): Default port changed from 9999 -> 8086
1. [#156](https://github.com/influxdata/influxdb-client-python/pull/156): Removed labels in organization API, removed Pkg* structure and package service

### Bug Fixes
1. [#154](https://github.com/influxdata/influxdb-client-python/pull/154): Fixed escaping string fields in DataFrame serialization

## 1.10.0 [2020-08-14]

### Features
1. [#140](https://github.com/influxdata/influxdb-client-python/pull/140): Added exponential backoff strategy for batching writes, Allowed to configure default retry strategy. Default value for `retry_interval` is 5_000 milliseconds.
1. [#136](https://github.com/influxdata/influxdb-client-python/pull/136): Allows users to skip of verifying SSL certificate
1. [#143](https://github.com/influxdata/influxdb-client-python/pull/143): Skip of verifying SSL certificate could be configured via config file or environment properties
1. [#141](https://github.com/influxdata/influxdb-client-python/pull/141): Added possibility to use datetime nanoseconds precision by `pandas.Timestamp`
1. [#145](https://github.com/influxdata/influxdb-client-python/pull/145): Api generator was moved to influxdb-clients-apigen

## 1.9.0 [2020-07-17]

### Features
1. [#112](https://github.com/influxdata/influxdb-client-python/pull/113): Support timestamp with different timezone in _convert_timestamp
1. [#120](https://github.com/influxdata/influxdb-client-python/pull/120): ciso8601 is an optional dependency and has to be installed separably
1. [#121](https://github.com/influxdata/influxdb-client-python/pull/121): Added query_data_frame_stream method
1. [#132](https://github.com/influxdata/influxdb-client-python/pull/132): Use microseconds resolutions for data points

### Bug Fixes
1. [#117](https://github.com/influxdata/influxdb-client-python/pull/117): Fixed appending default tags for single Point
1. [#115](https://github.com/influxdata/influxdb-client-python/pull/115): Fixed serialization of `\n`, `\r` and `\t` to Line Protocol, `=` is valid sign for measurement name
1. [#118](https://github.com/influxdata/influxdb-client-python/issues/118): Fixed serialization of DataFrame with empty (NaN) values
1. [#130](https://github.com/influxdata/influxdb-client-python/pull/130): Use `Retry-After` header value for Retryable error codes

## 1.8.0 [2020-06-19]

### Features
1. [#92](https://github.com/influxdata/influxdb-client-python/issues/92): Optimize serializing Pandas DataFrame for writing

### API
1. [#110](https://github.com/influxdata/influxdb-client-python/pull/110): Removed log system from Bucket, Dashboard, Organization, Task and Users API - [influxdb#18459](https://github.com/influxdata/influxdb/pull/18459), Update swagger to latest version

### Bug Fixes
1. [#105](https://github.com/influxdata/influxdb-client-python/pull/105): Fixed mapping dictionary without timestamp and tags into LineProtocol
1. [#108](https://github.com/influxdata/influxdb-client-python/pull/108): The WriteApi uses precision from Point instead a default precision

## 1.7.0 [2020-05-15]

### Features
1. [#79](https://github.com/influxdata/influxdb-client-python/issues/79): Added support for writing Pandas DataFrame

### Bug Fixes
1. [#85](https://github.com/influxdata/influxdb-client-python/issues/85): Fixed a possibility to generate empty write batch
2. [#86](https://github.com/influxdata/influxdb-client-python/issues/86): BREAKING CHANGE: Fixed parameters in delete api - now delete api accepts also bucket name and org name instead of only ids
1. [#93](https://github.com/influxdata/influxdb-client-python/pull/93): Remove trailing slash from connection URL

## 1.6.0 [2020-04-17]

### Documentation
1. [#75](https://github.com/influxdata/influxdb-client-python/issues/75): Updated docs to clarify how to use an org parameter
1. [#84](https://github.com/influxdata/influxdb-client-python/pull/84): Clarify how to use a client with InfluxDB 1.8

### Bug Fixes
1. [#72](https://github.com/influxdata/influxdb-client-python/issues/72): Optimize serializing data into Pandas DataFrame

## 1.5.0 [2020-03-13]

### Features
1. [#59](https://github.com/influxdata/influxdb-client-python/issues/59): Set User-Agent to influxdb-client-python/VERSION for all requests

### Bug Fixes
1. [#61](https://github.com/influxdata/influxdb-client-python/issues/61): Correctly parse CSV where multiple results include multiple tables
1. [#66](https://github.com/influxdata/influxdb-client-python/issues/66): Correctly close connection pool manager at exit
1. [#69](https://github.com/influxdata/influxdb-client-python/issues/69): `InfluxDBClient` and `WriteApi` could serialized by [pickle](https://docs.python.org/3/library/pickle.html#object.__getstate__) (python3.7 or higher)

## 1.4.0 [2020-02-14]

### Features
1. [#52](https://github.com/influxdata/influxdb-client-python/issues/52): Initialize client library from config file and environmental properties

### CI
1. [#54](https://github.com/influxdata/influxdb-client-python/pull/54): Add Python 3.7 and 3.8 to CI builds

### Bug Fixes
1. [#56](https://github.com/influxdata/influxdb-client-python/pull/56): Fix default tags for write batching, added new test
1. [#58](https://github.com/influxdata/influxdb-client-python/pull/58): Source distribution also contains: requirements.txt, extra-requirements.txt and test-requirements.txt

## 1.3.0 [2020-01-17]

### Features
1. [#50](https://github.com/influxdata/influxdb-client-python/issues/50): Implemented default tags

### API
1. [#47](https://github.com/influxdata/influxdb-client-python/pull/47): Updated swagger to latest version

### CI
1. [#49](https://github.com/influxdata/influxdb-client-python/pull/49): Added beta release to continuous integration

### Bug Fixes
1. [#48](https://github.com/influxdata/influxdb-client-python/pull/48): InfluxDBClient default org is used by WriteAPI

## 1.2.0 [2019-12-06]

### Features
1. [#44](https://github.com/influxdata/influxdb-client-python/pull/44): Optimized serialization into LineProtocol, Clarified how to use client for import large amount of data

### API
1. [#42](https://github.com/influxdata/influxdb-client-python/pull/42): Updated swagger to latest version

### Bug Fixes
1. [#45](https://github.com/influxdata/influxdb-client-python/pull/45): Pandas is a optional dependency and has to installed separably

## 1.1.0 [2019-11-19]

### Features
1. [#29](https://github.com/influxdata/influxdb-client-python/issues/29): Added support for serialise response into Pandas DataFrame

## 1.0.0 [2019-11-11]

### Features
1. [#24](https://github.com/influxdata/influxdb-client-python/issues/24): Added possibility to write dictionary-style object
1. [#27](https://github.com/influxdata/influxdb-client-python/issues/27): Added possibility to write bytes type of data
1. [#30](https://github.com/influxdata/influxdb-client-python/issues/30): Added support for streaming a query response
1. [#35](https://github.com/influxdata/influxdb-client-python/pull/35): FluxRecord supports dictionary-style access
1. [#31](https://github.com/influxdata/influxdb-client-python/issues/31): Added support for delete metrics

### API
1. [#28](https://github.com/bonitoo-io/influxdb-client-python/pull/28): Updated swagger to latest version

### Bug Fixes
1. [#19](https://github.com/bonitoo-io/influxdb-client-python/pull/19): Removed strict checking of enum values

### Documentation
1. [#22](https://github.com/bonitoo-io/influxdb-client-python/issues/22): Documented how to connect to InfluxCloud

## 0.0.2 [2019-09-26]

### Features
1. [#2](https://github.com/bonitoo-io/influxdb-client-python/issues/2): The write client is able to write data in batches (configuration: `batch_size`, `flush_interval`, `jitter_interval`, `retry_interval`)
1. [#5](https://github.com/bonitoo-io/influxdb-client-python/issues/5): Added support for gzip compression of query response and write body

### API
1. [#10](https://github.com/bonitoo-io/influxdb-client-python/pull/10): Updated swagger to latest version

### Bug Fixes
1. [#3](https://github.com/bonitoo-io/influxdb-client-python/issues/3): The management API correctly supports inheritance defined in Influx API
1. [#7](https://github.com/bonitoo-io/influxdb-client-python/issues/7): Drop NaN and infinity values from fields when writing to InfluxDB

### CI
1. [#11](https://github.com/bonitoo-io/influxdb-client-python/pull/11): Switch CI to CircleCI
1. [#12](https://github.com/bonitoo-io/influxdb-client-python/pull/12): CI generate code coverage report on CircleCI
