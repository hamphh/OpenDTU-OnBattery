FROM mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm

RUN apt-get update \
    && apt-get -qqy install \
        python3 \
        python3-dev \
        python3-distutils \
        python3-pip \
        python3-venv \
    # Clean up
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

RUN curl -fsSL -o get-platformio.py https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py
RUN python3 get-platformio.py