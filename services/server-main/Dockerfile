FROM node:24-alpine3.22
WORKDIR /app
COPY services/server-main/package* .
RUN npm install
COPY services/serveer-main/. .
COPY protos ./protos
ENV PORT=5001
EXPOSE 5001
CMD [ "node", "index.js" ]