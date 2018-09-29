---
layout: post
title: Day 67 of 100 Days Of Code
---

![VSCode](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/VSCode.png)

## Day 67: September 29, Saturday

**Today 's Progress**: Coded my local dev environment on my PC added Docker and tried to compiled a sample application.

**Thoughts**: Following this [Dockerize Vue.js App](https://vuejs.org/v2/cookbook/dockerize-vuejs-app.html)

### Resources used:
  * [Dockerize Vue.js App](https://vuejs.org/v2/cookbook/dockerize-vuejs-app.html)
  * [VueJS Tutorial](https://www.tutorialspoint.com/vuejs/index.htm)
  * [https://code.visualstudio.com/](https://code.visualstudio.com/)
  * [Webpack for vuejs](https://github.com/vuejs-templates/webpack)

```dockerfile
FROM node:9.11.1-alpine

# install simple http server for serving static content
RUN npm install -g http-server

# make the 'app' folder the current working directory
WORKDIR /app

# copy both 'package.json' and 'package-lock.json' (if available)
COPY package*.json ./

# install project dependencies
RUN npm install

# copy project files and folders to the current working directory (i.e. 'app' folder)
COPY . .

# build app for production with minification
RUN npm run build

EXPOSE 8080
CMD [ "http-server", "dist" ]
```


**Link(s) to work**

1. Started work on dockerizing my application local development Environment.

**Introduction to Vue.js**
Worked through setting up my local dev Environment

Code is at [https://github.com/Johnny2136/myproject](https://github.com/Johnny2136/myproject).
