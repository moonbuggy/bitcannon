FROM node:5

ADD . /var/www
WORKDIR /var/www

RUN npm install -g bower \
  && npm install -g grunt-cli \
  && rm -rf node_modules && rm -rf bower-components && rm -rf dist \
  && npm install
RUN bower install --allow-root=true --config.analytics=false --config.interactive=false
RUN grunt

EXPOSE 3000
CMD ["npm", "start"]
