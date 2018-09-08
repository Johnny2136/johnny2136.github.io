---
layout: post
title: Day 45 of 100 Days Of Code
---

!["JavaScript just got harder REACT/Redux!"](http://imgs.xkcd.com/comics/ui_change.png)

## Day 45: September 7, Friday

**Today 's Progress**: Continuing work on the React on Redux challenge, here we go back to misleading instructions and no examples! I knew it was too good to be true!!! The content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took a several hours to figure these out. First few weren't too bad, but the last one was pure hell! It had bad instructions no examples. I think these were written by different people. React and Redux would be easier to wrap my head around if there were more relevant examples. These challenges are getting slightly easier! once I got the solution the instructions sort of made sense but as I struggled I was cursing them!I think I was reading the instruction and trying to over think it. All I know is React and Redux are tough to get my head wrapped around.

### Resources used:
  * [GitHub react-redux Issues](https://github.com/reduxjs/react-redux/issues),
  * [Use Provider to Connect Redux to React](https://forum.freecodecamp.org/t/use-provider-to-connect-redux-to-react/202759)


  **Extract Local State into Redux**
  Once again back to misguiding instructions and no examples worked for a long time on this. TOTALLY TERRIBLE!
  * In the `Presentational` component, first, remove the `messages` property in the local `state`. These `messages` will be managed by Redux. Next, modify the `submitMessage()` method so that it dispatches `submitNewMessage()` from `this.props`, and pass in the current message input from local state as an argument. Because you removed messages from local state, remove the `messages` property from the call to `this.setState()` here as well. Finally, modify the `render()` method so that it maps over the messages received from `props` rather than `state`.

  * Once these changes are made, the app will continue to function the same, except Redux manages the `state`. This example also illustrates how a component may have local `state:` your component still tracks user input locally in its own `state`. You can see how Redux provides a useful state management framework on top of React. You achieved the same result using only React's local state at first, and this is usually possible with simple apps. However, as your apps become larger and more complex, so does your state management, and this is the problem Redux solves.


  ```Javascript
  // Redux:
  const ADD = 'ADD';
  const addMessage = (message) => {
    return {
      type: ADD,
      message: message
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
  // React:
  const Provider = ReactRedux.Provider;
  const connect = ReactRedux.connect;
  // Change code below this line
  class Presentational extends React.Component {
    constructor(props) {
      super(props);
      this.state = {
        input: '',
        //messages: []
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
      this.setState({
        input: '',
        //messages: this.state.messages.concat(this.state.input)
      });
      this.props.submitNewMessage(this.state.input);
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
            {this.props.messages.map((message, idx) => { //changed state to props
                return (
                   <li key={idx}>{message}</li>
                );
              })
            };
          </ul>
        </div>
      );
    };
  };
  // Change code above this line
  const mapStateToProps = (state) => {
    return {messages: state}
  };
  const mapDispatchToProps = (dispatch) => {
    return {
      submitNewMessage: (message) => {
        dispatch(addMessage(message))
      }
    }
  };
  const Container = connect(mapStateToProps, mapDispatchToProps)(Presentational);
  class AppWrapper extends React.Component {
    render() {
      return (
        <Provider store={store}>
          <Container/>
        </Provider>
      );
    }
  };
  ```
**Link(s) to work**

1. Continued work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (Trying to understand React on Redux)

**Introduction to the React and Redux Challenges**

* PassedMap State to Props
* PassedMap Dispatch to Props
* PassedConnect Redux to React
* PassedConnect Redux to the Messages App
* PassedExtract Local State into Redux

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).
