---
layout: post
title: Day 74 of 100 Days Of Code
---

![Saturday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging5.png)

## Day 74: October 06, Saturday

**Today 's Progress**: STILL Debugging (the CLI is hard. I can understand just putting script tags for vue in a html page and then codeing from there, but the CLI is a whole other beast.) [Vue.js Todo App - Basics - Part 1](https://www.youtube.com/watch?v=A5S23KS_-bU)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) to a local Git file and use Vue-CLI after going though more videos I am still struggleing to GROK this!!! Debugging continues.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles and renders... Without the list so more refactoring and debugging tomorrow.

```html
template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

```

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).
