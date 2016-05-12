# browsersync

[![](https://badge.imagelayers.io/blackxored/browsersync:latest.svg)](https://imagelayers.io/?images=blackxored/browsersync:latest)

Run [browsersync](http://browsersync.io/) inside a Docker container.
Exposes default port on 3000 and UI port on 3001.

## Why this image

This image is kept up to date with the latest NodeJS release (version 6 at the time),
and avoids common pitfalls with containerized Node processes failing to terminate
on Ctrl-C.

For the motivation itself, see my blog post [Improving dev environments: All the HTTP things](https://adrianperez.org/improving-dev-environments-all-the-http-things/)

## Usage

```shell
docker run --rm -it \
  -p 3000:3000 \
  -p 3001:3001 \
  -v "$(pwd)":/source \
  blackxored/browersync \
  start --server -files '**/*.css' --files '**/*.html'
```

Refer to BrowserSync documentation for a list of available command line options.

## License

For license information on the software included in this image, see
[BrowserSync LICENSE](https://github.com/BrowserSync/browser-sync/blob/master/LICENSE).

## Supported Docker versions

This image is officially supported on Docker version 1.11.1.

Please see the [Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade
your Docker daemon.

## User Feedback

### Issues

If you have any problems with or questions about this image, please make
contact through a [GitHub issue](https://github.com/blackxored/docker-browsersync/issues).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small;
we are always thrilled to receive pull requests, and do our best to process
them as fast as we can.

Before you start to code, we recommend discussing your plans through a GitHub
issue, especially for more ambitious contributions. This gives other
contributors a chance to point you in the right direction, give you feedback on
your design, and help you find out if someone else is working on the same
thing.

