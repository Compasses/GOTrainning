#  kingshard [中文主页](README_ZH.md)
[![Build Status](https://travis-ci.org/flike/kingshard.svg?branch=master)](https://travis-ci.org/flike/kingshard)

## Overview

kingshard is a high-performance proxy for MySQL powered by Go. Just like other mysql proxies, you can use it to split the read/write sqls. Now it supports basic SQL statements (select, insert, update, replace, delete). The most important feature is the sharding function. Kingshard aims to simplify the sharding solution of MySQL. **The Performance of kingshard is about 80% compared to connecting to MySQL directly.**

## Feature
- Splits reads and writes
- Support hash,range and date sharding across multiple nodes
- Client's ip ACL control.
- Transaction in single node.
- Support limitting the max count of connections to MySQL database.
- Support setting the backend database online or offline dynamically.
- Supports prepared statement: COM_STMT_PREPARE, COM_STMT_EXECUTE, etc.
- Support multi slaves, and loading banlance between slaves.
- Support reading master database forcely.
- Support sending sql to the specified node.
- Support most commonly used functions, such as `max, min, count, sum`, and also support `join, limit, order by,group by`.
- MySQL HA.
- Support set the charset of proxy.
- Support SQL blacklist.
- Support dynamically changing the config value of kingshard.

## Install
```
  1. Install Go
  2. git clone https://github.com/compasses/GOProjects/mysqlproxy.git src/github.com/compasses/GOProjects/mysqlproxy
  3. cd src/github.com/compasses/GOProjects/mysqlproxy
  4. source ./dev.sh
  5. make
  6. set the config file (etc/ks.yaml)
  7. run kingshard (./bin/kingshard -config=etc/ks.yaml)
```

# Details of kingshard

[1.How to use kingshard building a MySQL cluster](./doc/KingDoc/how_to_use_kingshard_EN.md)

## Donate

https://github.com/compasses/GOProjects/mysqlproxy/blob/master/doc/KingDoc/support.md

## License

kingshard is under the Apache 2.0 license. See the [LICENSE](./doc/License) directory for details.