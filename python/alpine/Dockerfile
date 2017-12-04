FROM python:3.6-alpine

ENV JSBEAUTIFIER_SHA256 7fc14f279117a55a5e854602f6e8c1cb178c6d83f7cf75e2e9f50678fe11079e

RUN set -ex; \
    apk add --no-cache --virtual .fetch-deps \
        ca-certificates \
        openssl \
        tar; \
    mkdir -p /usr/src/jsbeautifier; \
    wget -O jsbeautifier.tar.gz "https://pypi.python.org/packages/5b/cb/d4e4ec35f84cfcca9600cc5efa51e3e654828541437109f48ab85e61fbbe/jsbeautifier-1.7.4.tar.gz"; \
    echo "$JSBEAUTIFIER_SHA256  jsbeautifier.tar.gz" | sha256sum -c -; \
    tar --strip-components=1 -C /usr/src/jsbeautifier -xf jsbeautifier.tar.gz; \
    rm jsbeautifier.tar.gz; \
    pip install \
        --no-cache-dir \
        --disable-pip-version-check \
        /usr/src/jsbeautifier; \
    apk del .fetch-deps; \
    rm -rf /usr/src/jsbeautifier

ENTRYPOINT ["js-beautify"]
CMD ["-i"]
