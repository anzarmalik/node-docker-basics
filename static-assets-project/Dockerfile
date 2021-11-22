FROM node:12-stretch As build

WORKDIR /app

COPY . .

RUN npm ci && npm run build


FROM nginx:1.17

COPY --from=build  /app/build  /usr/share/nginx/html
