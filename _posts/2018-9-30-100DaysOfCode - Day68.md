---
layout: post
title: Day 68 of 100 Days Of Code
---

![sunday](http://blog.whooosreading.org/wp-content/uploads/2017/10/meditation.jpg)

## Day 68: September 30, Sunday

**Today 's Progress**: Gave up on Docker I have to have windows 10 pro and I do not have pro. So fell back 10 yards and punted. So onn with learning bu tutorials I am working through [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html).

**Thoughts**: Following these I am tring to add fetures and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/)

### Resources used:
  * [VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

```html
<div id="todoApp">
  <h2> {{message}} </h2>
  <p>
  New Tasks can be added below:
  </p>
  <form name="todo-form" method="post" action="" v-on:submit.prevent="addTask">
    <input name="add-todo" type="text" v-model="addTodoInput" v-bind:class="{error: hasError}"/>

    <button type="submit">Add</button>
  </form>

  <div class="todo-lists" v-if="lists.length"><br />
    <h3>My Todo Tasks:</h3>
    <ul>
      <li v-for="list in lists" :key="list.id">
        <input type="checkbox" v-on:change="completeTask(list)" v-bind:checked="list.isComplete"/>
        <del v-if="list.isComplete">
        {{list.title}}
        </del>
         <span v-else class="title" contenteditable="true" v-on:keydown.enter="updateTask($event, list)" v-on:blur="updateTask($event, list)" v-bind:class="{completed: list.isComplete}">{{list.title}}</span>
      </li>
    </ul>
  </div>
  <script>
  var todoApp = new Vue({
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
  </script>
```


**Link(s) to work**

1. Working on my TODO application jsfiddle.

Code is at [https://jsfiddle.net/johnny2136/g72evm4L/](https://jsfiddle.net/johnny2136/g72evm4L/).
