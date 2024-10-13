FROM kasmweb/kasm-core-kasmos
LABEL org.opencontainers.image.title="HamRadioUtils"
LABEL org.opencontainers.image.description="Ham Radio Utilities"
LABEL org.opencontainers.image.source="https://github.com/pcs3rd/kasm-images"
LABEL org.opencontainers.image.authors="pcs3rd"
LABEL org.opencontainers.image.vendor="pcs3rd"
LABEL org.opencontainers.image.licenses="GPL-3.0-only"

# Preinstall popular programming languages and package managers
RUN apt-get update && \
    apt-get install -y \
    hamradio-antenna hamradio-datamodes hamradio-digitalvoice hamradio-logging hamradio-morse hamradio-nonamateur hamradio-packetmodes hamradio-rigcontrol hamradio-satellite hamradio-sdr hamradio-tasks hamradio-tools hamradio-training

