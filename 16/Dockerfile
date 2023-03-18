FROM node:19.2.0-alpine3.15

LABEL maintainer "Leonardo Gatica <lgatica@protonmail.com>"

# Install build dependencies
# hadolint ignore=SC2034
RUN apk add --no-cache \
  build-base=0.5-r2 \
  curl=7.69.1-r1 \
  docker=19.03.12-r0 \
  git=2.26.2-r0 \
  jq=1.6-r1 \
  mysql-client=10.4.13-r0 \
  openssh-client=8.3_p1-r0 \
  py3-pip=20.1.1-r0 \
  python2=2.7.18-r0 && \
  npm i --unsafe-perm -g full-icu@1.3.1 now@19.1.2 && \
  npm i -g apollo@2.30.0 netlify-cli@2.63.2 surge@0.21.6 && \
  pip3 install awscli==1.18.97

ENV NODE_ICU_DATA=/usr/local/lib/node_modules/full-icu
