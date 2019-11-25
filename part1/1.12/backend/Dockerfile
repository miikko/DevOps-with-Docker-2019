FROM ubuntu

WORKDIR /backend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs
RUN npm install
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000

CMD npm start