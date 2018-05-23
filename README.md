# docker-grpcc

Runs [grpcc](https://github.com/njpatel/grpcc) in a container for easy querying of GPRC services.

## Usage

The `WORKDIR` is set to `/proto`. `--net="host"` allows docker to connect to your local machine on linux.

```
$ docker run --rm --net="host" -it -v `pwd`:/proto jfyne/grpcc -a 127.0.0.1:34000 -i -p service.proto
```
