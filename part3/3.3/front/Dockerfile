FROM ubuntu

WORKDIR /frontend
# Project should be pulled and placed in the same directory as this Dockerfile
COPY . . 
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m frontend && \
    chown -R frontend /frontend
USER frontend
EXPOSE 5000
ENV API_URL=http://localhost:8000

CMD npm start