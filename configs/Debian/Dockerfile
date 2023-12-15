FROM lscr.io/linuxserver/webtop:debian-xfce
LABEL org.opencontainers.image.authors="K.B.Dharun Krishna mail@kbdharun.dev"
LABEL org.opencontainers.image.description="This image is based on \
the Linuxserver.io Debian image using XFCE as the desktop environment \
along with additional packages of programming languages for development."
LABEL org.opencontainers.image.source="https://github.com/kbdharun/kasm-images"
LABEL org.opencontainers.image.title="Debian XFCE Dev"
LABEL org.opencontainers.image.vendor="kbdharun.dev"
LABEL org.opencontainers.image.licenses"="GPL-3.0-only"

# Preinstall popular programming languages and package managers
RUN apt-get update && \
    apt-get install -y \
    python3 python3-pip \
    curl wget git \
    gcc golang g++ make clang rust-all nodejs \
    meson ninja-build \
    jupyter-notebook
