# Alpine Linux standard

FROM youske/alpine-python:python3
MAINTAINER youske miyakoshi <youske@gmail.com>

LABEL com.stdmachine.description="alpine nodejs & python3 image" \
      com.stdmachine.role="nodejs & python3 image"

COPY package.json /tmp/
RUN apk add nodejs --no-cache && \
    apk add build-base linux-headers musl-dev nodejs-dev --no-cache -t buildpack && \
    cd /tmp && npm install -g && \
    apk del buildpack --no-cache && rm -rf /tmp/* /var/cache/apk/* /root/.wget-hsts
