# kasm-images

This repository contains my custom development images for [Kasm Workspaces](https://kasmweb.com) and webtop.

## Quick Reference

- **Compatible Kasm version** (for images): `1.14.0`.
- **Supported architecture**: `amd64`.
- **Registry**: <https://kbdharun.dev/kasm-workspaces-registry>.
- **Registry repo**: <https://github.com/kbdharun/kasm-workspaces-registry>.

## Images

> [!NOTE]
> The images in this repository are not official images and are not supported by Kasm Technologies. If you have any issues with these images, please open an issue in this repository and not upstream. All images are built with Linuxserver.io images as a base.

### Debian image

This image is based on the Linuxserver.io Debian image using XFCE as the desktop environment along with additional packages of programming languages for development.

Available via:

- GHCR (GitHub Container Registry): `ghcr.io/kbdharun/kasm-dev-debian:latest`
- DockerHub: `docker.io/kbdharun/kasm-dev-debian:latest`
- Quay: `quay.io/kbdharun/kasm-dev-debian:latest`

---

To verify the container image using [`cosign`](https://github.com/sigstore/cosign) (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR (GitHub Container Registry) image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-debian:latest
```

- For DockerHub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-debian:latest
```

- For Quay image:

```zsh
cosign verify --key cosign.pub quay.io/kbdharun/kasm-dev-debian:latest
```

### Ubuntu image

This image is based on the Linuxserver.io Ubuntu image using XFCE as the desktop environment along with additional packages of programming languages for development.

Available via:

- GHCR (GitHub Container Registry): `ghcr.io/kbdharun/kasm-dev-ubuntu:latest`
- DockerHub: `docker.io/kbdharun/kasm-dev-ubuntu:latest`
- Quay: `quay.io/kbdharun/kasm-dev-ubuntu:latest`

---

To verify the container image using [`cosign`](https://github.com/sigstore/cosign) (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR (GitHub Container Registry) image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-ubuntu:latest
```

- For DockerHub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-ubuntu:latest
```

- For Quay image:

```zsh
cosign verify --key cosign.pub quay.io/kbdharun/kasm-dev-ubuntu:latest
```

### Fedora image

There are two images based on the Linuxserver.io Fedora image. One uses XFCE as the desktop environment and the other uses KDE Plasma as the desktop environment. Both images have additional packages of programming languages for development.

Available via:

- GHCR (GitHub Container Registry): `ghcr.io/kbdharun/kasm-dev-fedora:latest` and `ghcr.io/kbdharun/kasm-dev-fedora-kde:latest`
- DockerHub: `docker.io/kbdharun/kasm-dev-fedora:latest` and `docker.io/kbdharun/kasm-dev-fedora-kde:latest`
- Quay: `quay.io/kbdharun/kasm-dev-fedora:latest` and `quay.io/kbdharun/kasm-dev-fedora-kde:latest`

---

To verify the container image using [`cosign`](https://github.com/sigstore/cosign) (download the `cosign.pub` file from [here](https://github.com/kbdharun/kasm-images/blob/main/cosign.pub) and execute the following command):

- For GHCR (GitHub Container Registry) image:

```zsh
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-fedora:latest
cosign verify --key cosign.pub ghcr.io/kbdharun/kasm-dev-fedora-kde:latest
```

- For DockerHub image:

```zsh
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-fedora:latest
cosign verify --key cosign.pub docker.io/kbdharun/kasm-dev-fedora-kde:latest
```

- For Quay image:

```zsh
cosign verify --key cosign.pub quay.io/kbdharun/kasm-dev-fedora:latest
cosign verify --key cosign.pub quay.io/kbdharun/kasm-dev-fedora-kde:latest
```

## Image Build Attestation

All the image builds/pushes are attested for provenanve and integrty using [`actions/attest-build-provenance`](https://github.com/actions/attest-build-provenance). They can be verfied by downloading the recent bundle from the [attestations page](https://github.com/kbdharun/kasm-images/attestations) and having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://<insert-image-url> --owner kbdharun --bundle <path/to/attestation_file.sigstore.json>
```

Where, `<insert-image-url>` is the URL of the image you want to verify (don't specify a tag) and `<path/to/attestation_file.sigstore.json>` is the path to the downloaded attestation file.

## Using as webtop

You can use these images as webtop by using the following [these steps](https://github.com/linuxserver/docker-webtop#usage) and replacing the image name with any image from this repository.
