FROM node:24-alpine3.22
WORKDIR /app
COPY services/moods-api/package* .
RUN npm install
COPY services/moods-api/. .
COPY protos ./protos
ENV PORT=5002
EXPOSE 5002
CMD [ "node", "index.js" ]