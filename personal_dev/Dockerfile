# Pull in the latest debian testing image.
# Not pinning a specific version since this is for personal dev inside distrobox.
FROM debian:testing

# Install a few packages I use for development.
#
# Base development tools.
RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    curl \
    man \
    git \
    git-lfs \
    graphviz \
    wget
# Python.
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-venv
# Node.
RUN apt-get update && apt-get install -y \
    npm
# Golang.
RUN apt-get update && apt-get install -y \
    golang-go
# Terminal tools.
RUN apt-get update && apt-get install -y \
    autojump \
    bash-completion \
    htop \
    ranger \
    tmux
# Security packages.
RUN apt-get update && apt-get install -y \
    openssl
# Networking tools.
RUN apt-get update && apt-get install -y \
    openssh-client \
    traceroute

# Editor.
RUN apt-get update && apt-get install -y \
    python3-neovim
# Install neovim from github since the debian version is very old.
RUN cd /usr && \
    curl -L https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz | \
        tar --strip-components=1 -z --extract -f -

# XXX
# - bazelisk
# - github CLI
# - onepass client

# XXX nvidia tools? dotfiles?
