FROM debian:jessie

RUN apt-get update -y
RUN apt-get install -y curl git
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash --
RUN apt-get install -y nodejs
RUN npm update -g npm
RUN npm cache clean --force
RUN npm i -g n
RUN n stable
RUN apt-get purge -y nodejs npm

ENTRYPOINT ["npm"]
CMD ["-h"]