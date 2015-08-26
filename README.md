
This repository contains configuration files for building a 
Docker (http://docker.io) image for the Subsonic media streamer.

Popmaïs Time
===============
Popmaïs is inspired of the famous [Popcorn Time](https://popcorntime.io).
But Popmaïs is implemented in Python. Popmaïs is technically simpler than Popcorn Time, so it's more portable and, I hope, easier to install. However, the content is identical.

***

<!-- ## Getting Involved
Want to report a bug, request a feature, contribute or translate Popcorn Time? Check out our in-depth guide to [Contributing to Popcorn Time](CONTRIBUTING.md). We need all the help we can get! You can also join in with our [community](README.md#community) to keep up-to-date and meet other Popcorn Timers. -->



## Difference with Popcorn Time
The major difference is that Popmaïs is a webapp, (run in any browser). Because Popcorn Time need many lib for GUI and that is the delicate point for the portability

## Getting Started

### Build your own image

```shell
$ docker build -t <your-name>/debian-subsonic debian-subsonic
```

### Get a pre-built image

A current image is available as a trusted build from the Docker index:

```shell
$ docker pull  loicent/popmais_time
```


## Run a container with this image

```shell
$ docker run \
  --detach \
  --publish 4040:4040 \
  --volume "/wherever/your/music/is:/var/music:ro" \
  <your-name>/debian-subsonic

```