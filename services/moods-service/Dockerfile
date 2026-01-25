FROM node:24-alpine3.22
WORKDIR /app
COPY services/moods-service/package* .
RUN npm install
COPY services/moods-service/. .
COPY protos ./protos
ENV PORT=50052
EXPOSE 50052
CMD [ "node", "index.js" ]