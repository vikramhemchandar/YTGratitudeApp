FROM node:24-alpine3.22
WORKDIR /app
COPY services/files-service/package* .
RUN npm install
COPY services/files-service/. .
COPY protos ./protos
ENV PORT=5004
EXPOSE 5004
CMD [ "node", "index.js" ]