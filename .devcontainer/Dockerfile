FROM mcr.microsoft.com/devcontainers/universal:2-linux
# Update packages
RUN apt-get update && apt-get install -y xz-utils \
    ca-certificates \
    gnupg \
    curl \
    xz-utils \
    software-properties-common
# Install node.js
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - && \
    apt-get install -y nodejs
# Install go
RUN curl -OL https://golang.org/dl/go1.21.6.linux-amd64.tar.gz && \
    tar -C /usr/local -xzf go1.21.6.linux-amd64.tar.gz && \
    echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/bash.bashrc