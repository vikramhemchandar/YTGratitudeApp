FROM node:24-alpine3.22
WORKDIR /app
COPY services/stats-service/package* .
RUN npm install
COPY services/stats-service/. .
COPY protos ./protos
ENV PORT=50053
EXPOSE 50053
CMD [ "node", "index.js" ]