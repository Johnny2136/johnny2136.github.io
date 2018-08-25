---
layout: post
title: Day 32 of 100 Days Of Code
---

![Image of reactjs](https://cdn-images-1.medium.com/max/1600/1*ZzZhMpsnsVPaFYLwZ0fs5g.jpeg)

## Day 31: August 24, Friday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: The React challenges for the most part so far have had very little relevant examples, and I guess I'm the only one struggling with this because there are very few students asking for help. I read the React Docs and did a bunch of google searches. I'm pretty sure I don't like React too much.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [repl.it/FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs)

```reactjs
//Use React to Render Nested Components
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};
const Fruits = () => {
  return (
    <div>
      { /* change code below this line */ }
      <TypesOfFruit />
      { /* change code above this line */ }
    </div>
  );
};
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  };
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* change code below this line */ }
        <Fruits />
        { /* change code above this line */ }
      </div>
    );
  };
};



//Compose React Components
class Fruits extends React.Component {
  constructor(props) {
    super(props);
  };
  render() {
    return (
      <div>
        <h2>Fruits:</h2>
        { /* change code below this line */ }
          <NonCitrus />
          <Citrus />
        { /* change code above this line */ }
      </div>
    );
  }
};
class TypesOfFood extends React.Component {
  constructor(props) {
     super(props);
  };
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* change code below this line */ }
          < Fruits />
        { /* change code above this line */ }
        <Vegetables />
      </div>
    );
  };
};



//Render a Class Component to the DOM
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* change code below this line */}
        < Fruits />
        < Vegetables />
        {/* change code above this line */}
      </div>
    );
  }
};
// change code below this line
 ReactDOM.render(<TypesOfFood />, document.getElementById('challenge-node'));
```

I'm pretty sure I don't like react at this point.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedRender HTML Elements to the DOM
* PassedDefine an HTML Class in JSX
* PassedLearn About Self-Closing JSX Tags
* PassedCreate a Stateless Functional Component
* PassedCreate a React Component
* PassedCreate a Component with Composition
* PassedUse React to Render Nested Components
* PassedCompose React Components
* PassedRender a Class Component to the DOM

All code is in GitHub and validated at repl.it here: [Repl.it/ Johnny's/ FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs) or [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
