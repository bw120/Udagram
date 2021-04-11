FROM node:12-alpine AS builder
WORKDIR /app
COPY . .
RUN npm install -g @ionic/cli
RUN npm install
RUN npm run build

# nginx for serving content
FROM nginx:alpine
WORKDIR /usr/share/nginx/html
# Remove default static assets
RUN rm -rf ./*

# Copy static assets from builder stage
COPY --from=builder /app/www .

# Containers run nginx with global directives and daemon off
ENTRYPOINT ["nginx", "-g", "daemon off;"]