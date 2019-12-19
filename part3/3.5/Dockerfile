FROM node:13-alpine as build-stage
WORKDIR /frontend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN npm install
RUN npm run build

FROM nginx:1-alpine
COPY --from=build-stage /frontend/dist/ /usr/share/nginx/html
ENV API_URL=http://localhost:8000
CMD ["nginx", "-g", "daemon off;"]
