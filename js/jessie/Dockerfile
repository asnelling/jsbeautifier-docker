FROM node:9

RUN set -ex; \
    yarn global add js-beautify@1.7.4; \
    yarn cache clean

ENTRYPOINT ["js-beautify"]
CMD ["-i"]
