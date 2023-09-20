FROM ubuntu

RUN apt-get update && apt-get install -y curl sudo

RUN curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -

RUN curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

RUN sudo apt-get install -y nodejs

#RUN sudo apt-get install -y yarn

RUN echo "NODE Version:" && node --version

RUN echo "NPM Version:" && npm --version

RUN mkdir /srv/app

RUN mkdir /srv/app/server

WORKDIR /srv/app/server

COPY . /srv/app/server

#COPY key.dat /

RUN npm install

RUN sudo npm install -g pm2

#RUN npm i cors

EXPOSE 3020

CMD npm start

#RUN NODE_ENV=production pm2 start index.js

#RUN npm start ecosystem.production.config.json

#CMD ["pm2-runtime", "NODE_ENV=production pm2 start index.js"]

#RUN pm2 start index.js

#CMD [ "node", "ecosystem.config.json" ]

#CMD ["npm start index.js", "start"]

#RUN NODE_ENV=production pm2 start index.js --name 'SmartInsuranceBackend'

#CMD ["pm2-runtime", "index.js"]

#CMD NODE_ENV=production pm2 start index.js --name SmartInsuranceBackend
