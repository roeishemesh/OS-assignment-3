# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.234.0/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT="bookworm"
FROM mcr.microsoft.com/devcontainers/base:${VARIANT}

# ** [Optional] Uncomment this section to install additional packages. **
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-linux-gnu binutils-riscv64-linux-gnu novnc websockify
# enable loading custom .gdbinit per folder.
# RUN echo set auto-load safe-path / > /root/.gdbinit
RUN echo set architecture riscv:rv64 > /root/.gdbinit