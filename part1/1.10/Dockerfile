FROM ubuntu

WORKDIR /frontend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs
RUN npm install
EXPOSE 5000
ENV API_URL=http://localhost:8000

CMD npm start