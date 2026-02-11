FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive
ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=1

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    git \
    curl \
    jq \
    zip \
    sudo \
    ca-certificates \
    libicu-dev \
    && rm -rf /var/lib/apt/lists/*

# Install only the Docker CLI (no daemon)
RUN curl -fsSL https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz | \
    tar xz --strip-components=1 -C /usr/local/bin docker/docker
