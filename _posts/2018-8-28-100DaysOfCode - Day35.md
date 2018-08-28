---
layout: post
title: Day 35 of 100 Days Of Code
---

## Day 35: August 28, Tuesday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges with no relevant examples. I don't see the benefit to the added complexity at all I am going to hate the projects for this.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [CodeSandbox](https://codesandbox.io/?from-app=1)

```reactjs
//Add Event Listeners
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: ''
    };
    this.handleEnter = this.handleEnter.bind(this);
    this.handleKeyPress = this.handleKeyPress.bind(this);
  }
  // change code below this line
  componentDidMount() {
    document.addEventListener('keydown', this.handleKeyPress)
  }
  componentWillUnmount() {
     document.removeEventListener('keydown', this.handleKeyPress)
  }
  // change code above this line
  handleEnter() {
    this.setState({
      message: this.state.message + 'You pressed the enter key! '
    });
  }
  handleKeyPress(event) {
    if (event.keyCode === 13) {
      this.handleEnter();
    }
  }
  render() {
    return (
      <div>
        <h3>Input Render:</h3>
        <p>{this.props.input}</p>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
};
```

A few relevant examples would be Awesome. I think I need to find a few good tutorials.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedCreate a Controlled Form
* PassedPass State as Props to Child Components
* PassedPass a Callback as Props
* PassedUse the Lifecycle Method componentWillMount
* PassedUse the Lifecycle Method componentDidMount
* PassedAdd Event Listeners
* PassedManage Updates with Lifecycle Methods

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
