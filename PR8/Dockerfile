
FROM node:18-alpine AS builder
WORKDIR /app


COPY package.json pnpm-lock.yaml ./
RUN npm install -g pnpm \
 && pnpm install


COPY . .
RUN pnpm run build


FROM nginx:stable-alpine

RUN rm -rf /usr/share/nginx/html/*


COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]