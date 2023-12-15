# kasm-images

This repository contains my custom development images for [Kasm Workspaces](https://kasmweb.com) (and webtop).

## Quick Reference

- **Compatible Kasm version** (for images): `1.14.0`.
- **Supported architecture**: `amd64`.
- **Registry**: <https://kbdharun.dev/kasm-workspaces-registry>.
- **Registry repo**: <https://github.com/kbdharun/kasm-workspaces-registry>.

## Images

> [!NOTE]
> The images in this repository are not official images and are not supported by Kasm Technologies. If you have any issues with these images, please open an issue in this repository and not upstream. All images are built with Linuxserver.io images as a base and are available in GHCR (GitHub Container Registry) and DockerHub.

The following images are available in this repository:

### Debian image

This image is based on the Linuxserver.io Debian image using XFCE as the desktop environment along with additional packages of programming languages for development.

To verify the integrity of the image using `cosign` (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-debian:latest
```

- For Docker Hub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-debian:latest
```

### Ubuntu image

This image is based on the Linuxserver.io Ubuntu image using XFCE as the desktop environment along with additional packages of programming languages for development.

To verify the integrity of the image using `cosign` (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-ubuntu:latest
```

- For Docker Hub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-ubuntu:latest
```

### Fedora image

There are two images based on the Linuxserver.io Fedora image. One uses XFCE as the desktop environment and the other uses KDE Plasma as the desktop environment. Both images have additional packages of programming languages for development.

To verify the integrity of the image using `cosign` (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-fedora:latest
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-fedora-kde:latest
```

- For Docker Hub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-fedora:latest
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-fedora-kde:latest
```

## Using as webtop

You can use these images as webtop by using the following [these steps](https://github.com/linuxserver/docker-webtop#usage) and replacing the image name with the image name from this repository.
