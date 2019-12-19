FROM node:13-alpine

WORKDIR /backend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN npm install && \
    chown -R node /backend
USER node
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000

CMD npm start