FROM ubuntu

COPY script.txt .
RUN chmod +x ./script.txt
RUN apt-get update && apt-get install -y wget && apt-get install -y curl

CMD "./script.txt"