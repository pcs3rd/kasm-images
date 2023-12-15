FROM lscr.io/linuxserver/webtop:debian-xfce
LABEL org.opencontainers.image.authors="K.B.Dharun Krishna mail@kbdharun.dev"

# Preinstall popular programming languages and package managers
RUN apt-get update && \
    apt-get install -y \
    python3 python3-pip \
    curl wget git \
    gcc golang g++ make clang rust-all nodejs \
    meson ninja-build \
    jupyter-notebook
