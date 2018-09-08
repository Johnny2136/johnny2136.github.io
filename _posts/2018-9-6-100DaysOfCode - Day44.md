---
layout: post
title: Day 44 of 100 Days Of Code
---

!["Not too bad!"](http://diasporina.com/wp/wp-content/uploads/2016/12/ntb.png)

## Day 44: September 6, Thursday

**Today 's Progress**: Continuing work on the React on Redux challenge instructions are starting to make more sense but examples are not accurate. I refuse to let this get to me!!! The content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took a couple hours to figure these out. First one was bad but the second one started making more sense! React and Redux would be easier to wrap my head around if there were more relevant examples. These challenges are getting slightly easier!

### Resources used:
  * [GitHub react-redux Issues](https://github.com/reduxjs/react-redux/issues),
  * [Use Provider to Connect Redux to React](https://forum.freecodecamp.org/t/use-provider-to-connect-redux-to-react/202759)


**Use Provider to Connect Redux to React**
This one wasn't too bad... (one change I would make is:)

*Example:*
```Javascript
render(){
    return(
      <Provider store={store}>
      <App/>
      </Provider>
    );
   };
   ```
The code editor now shows all your Redux and React code from the past several challenges. It includes the Redux store, actions, and the DisplayMessages component. The only new piece is the AppWrapper component at the bottom. Use this top level component to render the Provider from ReactRedux, and pass the Redux store as a prop. Then render the DisplayMessages component as a child. Once you are finished, you should see your React component rendered to the page.

Note: React Redux is available as a global variable here, so you can access the Provider with dot notation. The code in the editor takes advantage of this and sets it to a constant Provider for you to use in the AppWrapper render method.

[Can't get store from context #193](https://github.com/reduxjs/react-redux/issues/193)

```Javascript
// Redux Code:
const ADD = 'ADD';
const addMessage = (message) => {
  return {
    type: ADD,
    message
  }
};
const messageReducer = (state = [], action) => {
  switch (action.type) {
    case ADD:
      return [
        ...state,
        action.message
      ];
    default:
      return state;
  }
};
const store = Redux.createStore(messageReducer);

// React Code:
class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      messages: []
    }
    this.handleChange = this.handleChange.bind(this);
    this.submitMessage = this.submitMessage.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  submitMessage() {
    const currentMessage = this.state.input;
    this.setState({
      input: '',
      messages: this.state.messages.concat(currentMessage)
    });
  }
  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>
        <input
          value={this.state.input}
          onChange={this.handleChange}/><br/>
        <button onClick={this.submitMessage}>Submit</button>
        <ul>
          {this.state.messages.map( (message, idx) => {
              return (
                 <li key={idx}>{message}</li>
              )
            })
          }
        </ul>
      </div>
    );
  }
};
const Provider = ReactRedux.Provider;
class AppWrapper extends React.Component {
  // render the Provider here
    render(){
    return(
      <Provider store={store}>
        <DisplayMessages/>
      </Provider>
    );
  };
  // change code above this line
};
```
**Link(s) to work**

1. Continued work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (Trying to understand React on Redux)

**Introduction to the React and Redux Challenges**

* PassedExtract State Logic to Redux
* PassedUse Provider to Connect Redux to React

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).
