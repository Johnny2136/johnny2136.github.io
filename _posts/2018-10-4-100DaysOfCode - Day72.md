---
layout: post
title: Day 72 of 100 Days Of Code
---

![thursday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging3.png)

## Day 72: October 04, Thursday

**Today 's Progress**: STILL Debugging (But getting closer!!!! At least it compiles without errors!!!!) [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles but still doesn't render... continued debugging tomorrow.

```bash
johnn@DESKTOP-Johnny5 MINGW64 /d/johnny/GitHub/my-todo-app (feature)
$ npm run serve

> my-todo-app@0.1.0 serve D:\johnny\GitHub\my-todo-app
> vue-cli-service serve

 INFO  Starting development server...
 98% after emitting CopyPlugin

 DONE  Compiled successfully in 2725ms  9:10:56 PM  9:1 PM:10:56 PM
  App running at:
  - Local:   http://localhost:8081/
  - Network: http://192.168.56.1:8081/

  Note that the development build is not optimized.
  To create a production build, run npm run build.
```
The error I get in the browser is:
Uncaught ReferenceError: todoApp is not defined
    at eval (webpack-internal:///./node_modules/cache-loader/dist/cjs.js?!./node_modules/babel-loader/lib/index.js!./node_modules/cache-loader/dist/cjs.js?!./node_modules/vue-loader/lib/index.js?!./src/components/HelloWorld.vue?vue&type=script&lang=js&:82)
    at Module../node_modules/cache-loader/dist/cjs.js?!./node_modules/babel-loader/lib/index.js!./node_modules/cache-loader/dist/cjs.js?!./node_modules/vue-loader/lib/index.js?!./src/components/HelloWorld.vue?vue&type=script&lang=js& (app.js:829)
    at __webpack_require__ (app.js:725)
    at fn (app.js:102)
    at eval (webpack-internal:///./src/components/HelloWorld.vue?vue&type=script&lang=js&:2)
    at Module../src/components/HelloWorld.vue?vue&type=script&lang=js& (app.js:2046)
    at __webpack_require__ (app.js:725)
    at fn (app.js:102)
    at eval (webpack-internal:///./src/components/HelloWorld.vue:3)
    at Module../src/components/HelloWorld.vue (app.js:2034)
webpack-internal:///./node_modules/vue/dist/vue.runtime.esm.js:8009 You are running Vue in development mode.
Make sure to turn on production mode when deploying for production.
See more tips at https://vuejs.org/guide/deployment.html

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).
