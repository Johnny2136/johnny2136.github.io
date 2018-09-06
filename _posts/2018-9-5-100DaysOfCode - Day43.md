---
layout: post
title: Day 43 of 100 Days Of Code
---

![EXTREAM FRUSTRATION..."](https://fafysio.files.wordpress.com/2015/03/frustrert.gif)

## Day 43: September 5, Wednesday

**Today 's Progress**: I started work on the pure hell of React on Redux with misleading instructions and no examples Really frustrating stuff! The hellish content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took hours to figure these out. Worst of the worst! React and Redux would be easier to wrap my head around if there were accurate instructions and relevant examples these challenges are VERY hard!

### Resources used:
  * [Understanding unique keys for array children in React.js](https://stackoverflow.com/questions/28329382/understanding-unique-keys-for-array-children-in-react-js),
  * [React — to Bind or Not to Bind](https://medium.com/shoutem/react-to-bind-or-not-to-bind-7bf58327e22a)
  * [React and Redux: Manage State Locally First - freeCodeCamp Solution](https://www.youtube.com/watch?v=PPt0AS3RQ2Q)

  ## Getting Started with React Redux
  This should be a nice review of what you learned in the React lessons.(Just shoot me now!!!)
  Start with a DisplayMessages component. Add a constructor to this component and initialize it with a state that has two properties: input, that's set to an empty string, and messages, that's set to an empty array.
  [React Redux this.props.getClasses is not a function](https://stackoverflow.com/questions/50835770/react-redux-this-props-getclasses-is-not-a-function)
  ```javascript
  class DisplayMessages extends React.Component {
    // change code below this line
      constructor(props){
        super(props);
        this.state = {
          input:"",
          messages:[]
        }
      };    
    // change code above this line
    render() {
      return <div />
    }
  };
  ```

  ## React and Redux: Manage State Locally First
  WORST one YET!!!(Just shoot me now!!!)
  * First, in the render() method, have the component render an input element, button element, and ul element. When the input element changes, it should trigger a handleChange() method. Also, the input element should render the value of input that's in the component's state. The button element should trigger a submitMessage() method when it's clicked.

  * Second, write these two methods. The handleChange() method should update the input with what the user is typing. The submitMessage() method should concatenate the current message (stored in input) to the messages array in local state, and clear the value of the input.

  * Finally, use the ul to map over the array of messages and render it to the screen as a list of li elements.
  * [React Redux youTube Video on this challange](https://www.youtube.com/watch?v=PPt0AS3RQ2Q)
  ```javascript
  class DisplayMessages extends React.Component {
    constructor(props) {
      super(props);
      this.state = {
        input: '',
        messages: []
      }
      this.handleChange=this.handleChange.bind(this)//had to bind handleChange
      this.submitMessage=this.submitMessage.bind(this)//had to bind submitMessage
    }
    // add handleChange() and submitMessage() methods here
    handleChange(event){
      this.setState({
        input: event.target.value
      })    
    }
    submitMessage(){
      this.setState({
        messages: [...this.state.messages,this.state.input],
        input: ''
      })    
    }
    render() {
      return (
        <div>
          <h2>Type in a new Message:</h2>
          { /* render an input, button, and ul here */ }
            <input value={this.state.input} onChange={this.handleChange}/>

            <button onClick={this.submitMessage}>Submit</button>
            <ul>
            {this.state.messages.map(message => <li key={Date}>{message}</li>)}
            </ul>
          { /* change code above this line */ }
        </div>
      );
    }
  };
  ```
**Link(s) to work**

1. Started work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (trying to) learn React on Redux.

**Introduction to the React Challenges**

* PassedGetting Started with React Redux
* PassedManage State Locally First

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).
