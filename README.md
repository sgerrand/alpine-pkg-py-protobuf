# alpine-pkg-py-protobuf

[![CircleCI](https://img.shields.io/circleci/project/sgerrand/alpine-pkg-py-protobuf/master.svg)](https://circleci.com/gh/sgerrand/alpine-pkg-py-protobuf)

This is the [Python protobuf][py-protobuf] package as an Alpine Linux package.

## Releases

See the [releases page][releases] for the latest download links.

## Installing

The current installation method for these packages is to pull them in using
`wget` or `curl` and install the local file with the `--allow-untrusted` option
to `apk`:

```
apk --no-cache add ca-certificates
wget https://github.com/sgerrand/alpine-pkg-py-protobuf/releases/download/2.6.1-r0/py-protobuf-2.6.1-r0.apk
apk --allow-untrusted add py-protobuf-2.6.1-r0.apk
```

[py-protobuf]: https://pypi.python.org/pypi/protobuf
[releases]: https://github.com/sgerrand/alpine-pkg-py-protobuf/releases/
