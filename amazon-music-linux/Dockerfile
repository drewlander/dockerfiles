FROM ubuntu:18.04

RUN apt-get update && apt-get install -y curl gnupg2 wget
RUN wget https://github.com/oja/amazon-music-linux/releases/download/v.1.4.0/amazon-music-linux-1.4.0_amd64.deb
RUN apt install -y  ./amazon-music-linux-1.4.0_amd64.deb
ENTRYPOINT ["/usr/bin/amazon-music-linux"]

