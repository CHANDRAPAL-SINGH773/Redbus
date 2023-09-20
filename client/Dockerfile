FROM ubuntu
RUN apt-get update && apt-get install -y curl sudo
RUN curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
RUN sudo apt-get install -y nodejs
RUN echo "NODE Version:" && node --version
RUN echo "NPM Version:" && npm --version
RUN mkdir /srv/app
RUN mkdir /srv/app/client
WORKDIR /srv/app/client
COPY . /srv/app/client
RUN npm install
CMD npm start
EXPOSE 3000
