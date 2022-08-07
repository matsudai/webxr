FROM node:16.16.0-bullseye-slim

#
# 1. Install packages.
#
#     1. Utilities.
#         - curl
#         - git
#         - vim
#
#     2. Locale.
#         - locales
#
RUN apt update && \
    apt install -y \
        curl git vim \
        locales \
        && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

#
# 2. Locale.
#
# Default locale = ja_JP
#
RUN locale-gen ja_JP.UTF-8 && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8

USER node

EXPOSE 3000
