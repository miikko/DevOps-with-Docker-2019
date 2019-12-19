FROM node:13-alpine

WORKDIR /frontend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN npm install && \
    chown -R node /frontend
USER node
EXPOSE 5000
ENV API_URL=http://localhost:8000

CMD npm start