---
layout: post
title: Day 73 of 100 Days Of Code
---

![friday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging4.png)

## Day 73: October 05, Friday

**Today 's Progress**: STILL Debugging (back to compiling with errors!!!!) [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles but still doesn't render... continued debugging tomorrow.

```html
<li v-for="todo in todos">
     <label>
       <input type="checkbox"
         v-on:change="toggle(todo)"
         v-bind:checked="todo.done">

       <del v-if="todo.done">
         {{ todo.text }}
       </del>
       <span v-else>
         {{ todo.text }}
       </span>
     </label>
   </li>
 </div>
```
The error I get in the browser is:
![error](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Error4forDebugging4.png)

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).
