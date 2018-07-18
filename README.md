# docker-grpcc

Runs [grpcc](https://github.com/njpatel/grpcc) in a container for easy querying of GPRC services.

This image includes common proto libraries from [znly/docker-protobuf](https://github.com/znly/docker-protobuf).

## Usage

The `WORKDIR` is set to `/proto`. Mount your proto file here to have it available.

On Linux `--net="host"` allows docker to connect to your local machine.
On a Mac use `host.docker.internal` to connect back to your own host.

```
$ docker run --rm --net="host" -it -v `pwd`:/proto jfyne/grpcc -a 127.0.0.1:34000 -i -p service.proto
```
