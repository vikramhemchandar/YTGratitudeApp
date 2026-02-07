FROM node:24-alpine3.22
WORKDIR /app
COPY services/stats-api/package* .
RUN npm install
COPY services/stats-api/. .
COPY protos ./protos
ENV PORT=5003
EXPOSE 5003
CMD [ "node", "index.js" ]