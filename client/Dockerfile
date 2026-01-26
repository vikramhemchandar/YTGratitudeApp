FROM node:24-alpine3.22 AS build
WORKDIR /app
COPY client/package* .
RUN npm install
COPY client/. .
RUN npm run build

FROM nginx:stable-alpine AS prod
COPY --from=build /app/build /usr/share/nginx/html
COPY nginx.conf /opt/homebrew/etc/nginx/
EXPOSE 80
CMD [ "nginx", "-g", "daemon off;" ]
