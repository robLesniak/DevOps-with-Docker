FROM ubuntu:16.04

RUN mkdir -p /var/www/app
WORKDIR /var/www/app
RUN apt-get update && apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN apt-get install --assume-yes git
RUN git clone https://github.com/docker-hy/frontend-example-docker.git
WORKDIR  /var/www/app/frontend-example-docker
RUN npm install
EXPOSE 5000
CMD ["npm", "start"]
 



