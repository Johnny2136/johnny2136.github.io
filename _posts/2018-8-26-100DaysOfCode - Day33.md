---
layout: post
title: Day 33 of 100 Days Of Code
---

![Image of one third](https://static.abcteach.com/free_preview/f/fractions_1third_rgb_p.png)

## Day 33: August 26, Sunday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Again the React challenges have had very little relevant examples, and I'm not the only one struggling with this because now I see there are a few more students asking for help. I read the React Docs and did a bunch of google searches. I'm pretty sure I don't like React too much. Also the sand box for react is problematic.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [repl.it/FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs)

```reactjs
//Override Default Props
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
}
Items.defaultProps = {
  quantity: 0
}
class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    { /* change code below this line */ }
    return (
      <Items quantity = {10} />);
    { /* change code above this line */ }
  }
};
```

I'm really sure I don't like react at this point.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedWrite a React Component from Scratch
* PassedPass Props to a Stateless Functional Component
* PassedPass an Array as Props
* PassedUse Default Props
* PassedOverride Default Props

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
