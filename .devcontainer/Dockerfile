FROM node:24-slim

# Basic tools commonly needed during development.
RUN apt-get update \
  && apt-get install -y --no-install-recommends git ca-certificates openssh-client \
  && rm -rf /var/lib/apt/lists/*

ENV PNPM_HOME=/home/node/.local/share/pnpm
ENV PATH=${PNPM_HOME}:${PATH}
ENV COREPACK_ENABLE_DOWNLOAD_PROMPT=0

# Enable pnpm through Corepack in the image so every container starts ready.
RUN corepack enable && corepack prepare pnpm@11.9.0 --activate

USER node
