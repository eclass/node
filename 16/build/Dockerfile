FROM node:16.13.2-alpine3.15

LABEL maintainer "Leonardo Gatica <lgatica@protonmail.com>"

# Install build dependencies
RUN apk add --no-cache \
  build-base=0.5-r2 \
  git=2.26.2-r0 \
  openssh-client=8.3_p1-r0 \
  python2=2.7.18-r0 && \
  # Create ssh directory
  mkdir ~/.ssh && \
  chmod 0600 ~/.ssh && \
  # Add gitlab.com to known_hosts
  ssh-keyscan gitlab.com > ~/.ssh/known_hosts

WORKDIR /usr/src/app
