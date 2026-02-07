FROM node:20-bullseye-slim
WORKDIR /app
COPY services/server-main/package* .
RUN npm install
COPY services/server-main/. .
COPY protos ./protos
ENV PORT=5001
EXPOSE 5001
CMD [ "node", "start" ]