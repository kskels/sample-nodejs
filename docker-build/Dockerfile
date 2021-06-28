# From https://github.com/SaschaSchwarze0/npm-simple
FROM registry.access.redhat.com/ubi8/nodejs-12

USER 0

COPY . /app
RUN cd /app && \
    pwd && \
    ls -l && \
    npm install && \
    npm run print-http-server-version

RUN chown -R 1001:0 /app

WORKDIR /app
EXPOSE 8080

USER 1001
CMD ["npm", "start"]
