FROM node:19.2.0-alpine3.15

LABEL maintainer "Leonardo Gatica <lgatica@protonmail.com>"

ENV TZ=America/Santiago NODE_ENV=production PORT=3000

# App directory
RUN mkdir /home/node/app/ && chown -R node:node /home/node/app
WORKDIR /home/node/app

# Add HEALTHCHECK
RUN npm i -g healthcheck-cli@1.0.1 \
  # Add IANA TZ database
  tzdata@1.0.19 && \
  # Add full ICU data
  npm i --unsafe-perm -g full-icu@1.3.1

# Set healthcheck *.test.js/healthcheck
HEALTHCHECK --interval=5m --timeout=3s \
  CMD healthcheck 127.0.0.1 3000 /healthcheck

# Set ICU data path
ENV NODE_ICU_DATA="/usr/local/lib/node_modules/full-icu"

USER node
