FROM node:16.18.1-alpine3.15

LABEL maintainer "Developer eClass <developer@eclass.cl>"

# Install build dependencies
# hadolint ignore=SC2034
RUN apk add --no-cache \
  build-base=0.5-r3 \
  curl=8.5.0-r0 \
  docker=20.10.16-r0 \
  git=2.34.8-r0 \
  jq=1.6-r1 \
  mysql-client=10.6.14-r0 \
  openssh-client-default=8.8_p1-r1 \
  py3-pip=20.3.4-r1 \
  python2=2.7.18-r4 && \
  npm i --unsafe-perm -g full-icu@1.3.1 now@19.1.2 && \
  npm i -g apollo@2.30.0 netlify-cli@2.63.2 surge@0.21.6 && \
  pip3 install awscli==1.18.97

ENV NODE_ICU_DATA=/usr/local/lib/node_modules/full-icu
