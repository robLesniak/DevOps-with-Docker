FROM ubuntu:16.04
RUN mkdir -p /var/www/appback
WORKDIR /var/www/appback
RUN apt-get update && apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN apt-get install --assume-yes git
RUN git clone https://github.com/docker-hy/backend-example-docker.git
WORKDIR /var/www/appback/backend-example-docker
RUN npm install
EXPOSE 8000
ENV FRONT_URL=http://localhost:5000
CMD ["npm", "start"]

