---
layout: post
title: Day 75 of 100 Days Of Code
---

![Sunday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging6.png)

## Day 75: October 07, Sunday

**Today 's Progress**: Making headway on my Vue todo app slow progress but progress none the less [Vue.js Todo App - Basics - Part 1](https://www.youtube.com/watch?v=A5S23KS_-bU)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, Working somewhat...

**Thoughts**: I am tiring to add my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) to a local Git file and use Vue-CLI 3.0 after going though more videos I am still struggling but starting to get it, cautiously optimistic. Debugging continues.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles renders and shows tasks... more refactoring and debugging tomorrow. PROGRESS!!!!

```html
<template>
<div>
    <h2> My Vue.JS ToDo List:</h2>
     <input type="text" class="todo-input" placeholder="Add what needs to be done here!" v-model="newTodo" @keyup.enter="addTodo">     
      <div v-for="todo in todos" :key="todo.id" class="todo-item">
        {{todo.title}}
      </div>
</div>
</template>
<script>
/* eslint-disable */
export default {
  name: 'todo-list',
  data () {
    return {
        newTodo: '',
        idForTodo: 3,
        beforeEditCache: '',
        filter: 'all',
        todos: [
        {
          'id': 1,
          'title': 'Finish Vue ToDo Project',
          'completed': false,
          'editing': false,
        },
        {
          'id': 2,
          'title': 'Grok Vue-CLI',
          'completed': false,
          'editing': false,
        },
      ]
    }
  },
  methods: {
    addTodo() {
      //alert('adding todo')
      if (this.newTodo.trim().length == 0) {
        return
      }
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
        editing: false,
      })
      this.newTodo = ''
      this.idForTodo++
    },
  },
 }

</script>
<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css");
  .todo-input {
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;
    &:focus {
      outline: 0;
    }
  }
  .todo-item {
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    animation-duration: 0.3s;
  }
  .remove-item {
    cursor: pointer;
    margin-left: 14px;
    &:hover {
      color: black;
    }
  }
  .todo-item-left { // later
    display: flex;
    align-items: center;
  }
  .todo-item-label {
    padding: 10px;
    border: 1px solid white;
    margin-left: 12px;
  }
  .todo-item-edit {
    font-size: 24px;
    color: #2c3e50;
    margin-left: 12px;
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc; //override defaults
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    &:focus {
      outline: none;
    }
  }
  .completed {
    text-decoration: line-through;
    color: grey;
  }
  .extra-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 16px;
    border-top: 1px solid lightgrey;
    padding-top: 14px;
    margin-bottom: 14px;
  }
  button {
    font-size: 14px;
    background-color: white;
    appearance: none;
    &:hover {
      background: lightgreen;
    }
    &:focus {
      outline: none;
    }
  }
  .active {
    background: lightgreen;
  }
  // CSS Transitions
  .fade-enter-active, .fade-leave-active {
    transition: opacity .2s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
</style>
```

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).
