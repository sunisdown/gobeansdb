# GoBeansDB [![Build Status](https://travis-ci.org/douban/gobeansdb.svg?branch=master)](https://travis-ci.org/douban/gobeansdb) 

Yet anonther distributed key-value storage system from Douban Inc.

Any memcached client cache interactive with GobeansDB without any modification.

# Prepare

GoBeansDB use `vgo` manage dependencies, please install vgo first.


# Install

```shell
$ cd ${GOPATH}
$ git clone http://github.com/douban/gobeansdb.git src/github.com/douban/gobeansdb
$ cd src/github.com/douban/gobeansdb
$ make
```

# test

```shell
$ make test  # unit test
$ make pytest  # Integrated test
```

# run

```shell
$ ${GOPATH}/bin/gobeansdb -h
```

# Python Example

```
import libmc


mc = libmc.Client(['localhost:7900'])
mc.set("foo", "bar")
mc.get("foo")

```
