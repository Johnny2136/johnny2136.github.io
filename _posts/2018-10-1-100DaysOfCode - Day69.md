---
layout: post
title: Day 69 of 100 Days Of Code
---

![Monday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/LocalToDo.png)

## Day 69: October 01, Monday

**Today 's Progress**: I am working through getting [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment.

**Thoughts**: Following these I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)
Errors in... debugging tomorrow.
```javascript
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'
import router from './router'

Vue.config.productionTip = false

/* eslint-disable no-new */
  var app = new Vue({
    el: '#todoApp',
    data: {
      message: 'Welcome to Todo App',
      addTodoInput: '',
      lists: [],
      hasError: false
    },
    methods:{
      addTask(){

        if(!this.addTodoInput){
          this.hasError = true;
          return;
        }

        this.hasError = false;

        this.lists.push({
          id:this.lists.length+1,
          title: this.addTodoInput,
          isComplete: false
        });

        this.addTodoInput = '';
      },

      updateTask(e, list){
        e.preventDefault();
        list.title = e.target.innerText;
        e.target.blur();
      },

      completeTask(list){
        list.isComplete = !list.isComplete;
      }

    }
  });

  //generate dummy data for demo purpose
  todoApp.lists = [{
        id: 1,
        title: "Hello Vue.JS",
        isComplete: false
      },
      {
        id: 2,
        title: "Learn JavaScript",
        isComplete: false
      },
      {
        id: 3,
        title: "Learn Vue",
        isComplete: false
      },
      {
        id: 4,
        title: "Play around in JSFiddle",
        isComplete: true
      }];
```


**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).
