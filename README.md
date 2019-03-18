# shairport-sync-docker-pi

A Docker image to run [shairport-sync](https://github.com/mikebrady/shairport-sync) on a Raspberry Pi.

Tested on a Raspberry Pi 3 running Debian Jessie.

[Dockerhub](https://hub.docker.com/r/pm6422/shairport-sync-docker-pi/): [![](https://images.microbadger.com/badges/version/pm6422/shairport-sync-docker-pi.svg)](https://microbadger.com/images/pm6422/shairport-sync-docker-pi "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/pm6422/shairport-sync-docker-pi.svg)](https://microbadger.com/images/pm6422/shairport-sync-docker-pi "Get your own image badge on microbadger.com") 

# Usage

## From Dockerhub (Recommended)

```sh
$ docker run -d \
            --name airplay \
            --net host \
            --device /dev/snd \
            pm6422/shairport-sync-docker-pi
```

## Building from scratch

```sh
$ git clone https://github.com/pm6422/shairport-sync-docker-pi.git/
$ cd shairport-sync-docker-pi
$ docker build . -t shairport-sync-docker-pi
$ docker run -d \
            --name airplay \
            --net host \
            --device /dev/snd \
            pm6422/shairport-sync-docker-pi
```

---

The server will now show up on your macOS and iOS devices and you should be able to play music to them.

NOTE: In it's current form, sound may not be output through the Raspberry Pi's headphone jack.  It has only been tested with HDMI output.
