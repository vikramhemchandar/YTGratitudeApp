FROM node:24-alpine3.22
WORKDIR /app
COPY services/entries-service/package* .
RUN npm install
COPY services/entries-service/. .
COPY protos ./protos
ENV PORT=50051
EXPOSE 50051
CMD [ "node", "index.js" ]