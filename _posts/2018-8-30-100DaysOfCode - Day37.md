---
layout: post
title: Day 37 of 100 Days Of Code
---

## Day 37: August 30, Thursday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges I did find some examples through google. I endeavor to persevere. Tonight it was pretty hard I hope this helps with [React: Render Conditionally from Props](https://learn.freecodecamp.org/front-end-libraries/react/render-conditionally-from-props)

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Render Conditionally from Props
//This was totally awful... poor instructions, no good examples, took a long time to get this.
class Results extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
   /* change code here ALSO!!! (but this isn't in the original setup!) */
   const { fiftyFifty } = this.props;
    return (
      <h1>
      {
        /* change code here */
        fiftyFifty ? 'You Win!' : 'You Lose!'
      }
      </h1>
    )
  };
};
class GameOfChance extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      counter: 1
    }
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({
      counter: this.state.counter + 1 // change code here "this.state.counter + 1"
    });
  }
  render() {
    let expression = Math.random() > .5; // change code here "Math.random() > .5;"
    return (
      <div>
        <button onClick={this.handleClick}>Play Again</button>
        { /* change code below this line */ }
          <Results fiftyFifty={expression} /> //And lastly here!
        { /* change code above this line */ }
        <p>{'Turn: ' + this.state.counter}</p>
      </div>
    );
  }
};
```

This was a VERY hard one, instructions were not very clear I hope this helps someone who is struggling like I was.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedUse && for a More Concise Conditional
* PassedUse a Ternary Expression for Conditional Rendering
* PassedRender Conditionally from Props

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
