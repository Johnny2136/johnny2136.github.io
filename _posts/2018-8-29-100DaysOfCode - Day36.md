---
layout: post
title: Day 36 of 100 Days Of Code
---

## Day 36: August 29, Wednesday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges I did find some examples on google. I endeavor to persevere.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Use Advanced JavaScript in React Render Method
//An example would have been nice!
const inputStyle = {
  width: 235,
  margin: 5
}
class MagicEightBall extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      userInput: '',
      randomIndex: ''
    }
    this.ask = this.ask.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }
  ask() {
    if (this.state.userInput) {
      this.setState({
        randomIndex: Math.floor(Math.random() * 20),
        userInput: ''
      });
    }
  }
  handleChange(event) {
    this.setState({
      userInput: event.target.value
    });
  }
  render() {
    const possibleAnswers = [
      'It is certain',
      'It is decidedly so',
      'Without a doubt',
      'Yes, definitely',
      'You may rely on it',
      'As I see it, yes',
      'Outlook good',
      'Yes',
      'Signs point to yes',
      'Reply hazy try again',
      'Ask again later',
      'Better not tell you now',
      'Cannot predict now',
      'Concentrate and ask again',
      'Don\'t count on it',
      'My reply is no',
      'My sources say no',
      'Most likely',
      'Outlook not so good',
      'Very doubtful'
    ];
    const answer = possibleAnswers[this.state.randomIndex] // << change code here
    return (
      <div>
        <input
          type="text"
          value={this.state.userInput}
          onChange={this.handleChange}
          style={inputStyle} /><br />
        <button onClick={this.ask}>
          Ask the Magic Eight Ball!
        </button><br />
        <h3>Answer:</h3>
        <p>
          { /* change code below this line */ }
          {answer}
          { /* change code above this line */ }
        </p>
      </div>
    );
  }
};
```

This could be a good example for framework for the random quote machine.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedOptimize Re-Renders with shouldComponentUpdate
* PassedIntroducing Inline Styles
* PassedAdd Inline Styles in React
* PassedUse Advanced JavaScript in React Render Method

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
