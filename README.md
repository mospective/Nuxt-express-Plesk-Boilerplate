# boilerplate-nuxt-express

> Plesk Ready Nuxt.js App with Express.js Server

## Build Setup

``` bash
# install dependencies
$ npm run install

# serve with hot reload at localhost:3000 - this best used when using express.js api
$ npm run dev

# Alternatively at localhost:3000 it will open in default browser with reload
$ npm run begin

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

Useful links: https://nuxtjs.org/faq/postcss-plugins/
https://nuxtjs.org/api/configuration-build/


### Uploading to plesk
Link to deploying to plesk: https://raoulkramer.de/deploy-a-nuxt-js-application-on-a-plesk-onyx-v-server-as-node-js-application/

Under Enable additional Deploy action: 
``` bash
$ /opt/plesk/node/12/bin/npm ci --scripts-prepend-node-path
$ /opt/plesk/node/12/bin/npm run build --scripts-prepend-node-path
$ touch tmp/restart.txt
```
If you get a node error, create .npmrc file with the following:
``` bash
$ scripts-prepend-node-path=true
```
Upload file to the root folder in plesk
