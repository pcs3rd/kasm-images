FROM lscr.io/linuxserver/webtop:ubuntu-xfce
LABEL org.opencontainers.image.authors="K.B.Dharun Krishna mail@kbdharun.dev"
LABEL description="This image is based on \
the Linuxserver.io Ubuntu image using XFCE as the desktop environment \
along with additional packages of programming languages for development."

# Preinstall popular programming languages and package managers
RUN apt-get update && \
    apt-get install -y \
    python3 python3-pip \
    curl wget git \
    gcc golang g++ make clang \
    rust-all nodejs \
    meson ninja-build \
    jupyter-notebook libreoffice
