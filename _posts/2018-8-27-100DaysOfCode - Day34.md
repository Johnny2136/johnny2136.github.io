---
layout: post
title: Day 34 of 100 Days Of Code
---

## Day 34: August 27, Monday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: The React challenges have hardly no relevant examples, Would it kill them to put in some relevant examples??? I read the React Docs and tutorials. I just don't see the benefit to the added complexity.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [CodeSandbox](https://codesandbox.io/?from-app=1)

```reactjs
//Review Using Props with Stateless Functional Components
//NO GOOD EXAMPLE!!!
class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <Camper name='camper' />
      </div>
    );
  }
};
// change code below this line
class Camper extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <p>{this.props.name}</p>
    );
  }
};
Camper.propTypes = {name:PropTypes.string.isRequired};
Camper.defaultProps = { name : 'CamperBot'};
```

A few relevant examples would be nice.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedUse PropTypes to Define the Props You Expect
* PassedAccess Props Using this.props
* PassedReview Using Props with Stateless Functional Components
* PassedCreate a Stateful Component
* PassedRender State in the User Interface
* PassedRender State in the User Interface Another Way
* PassedSet State with this.setState
* PassedBind 'this' to a Class Method
* PassedUse State to Toggle an Element
* PassedWrite a Simple Counter
* PassedCreate a Controlled Input

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
