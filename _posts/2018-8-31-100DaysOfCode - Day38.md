---
layout: post
title: Day 38 of 100 Days Of Code
---

## Day 38: August 31, Friday

**Today 's Progress**: I finally finished React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: I AM SO HAPPY the React challenges are finally done. I don't like ReactJS

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Give Sibling Elements a Unique Key Attribute
const frontEndFrameworks = [
  'React',
  'Angular',
  'Ember',
  'Knockout',
  'Backbone',
  'Vue'
];
function Frameworks() {
  // change code here
  const renderFrameworks = frontEndFrameworks.map((renderFrameworks) => <li key={renderFrameworks.toString()}>{renderFrameworks}</li>)
  return (
    <div>
      <h1>Popular Front End JavaScript Frameworks</h1>
      <ul>
        {renderFrameworks}
      </ul>
    </div>
  );
};



//Use Array.filter() to Dynamically Filter an Array
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      users: [
        {
          username: 'Jeff',
          online: true
        },
        {
          username: 'Alan',
          online: false
        },
        {
          username: 'Mary',
          online: true
        },
        {
          username: 'Jim',
          online: false
        },
        {
          username: 'Sara',
          online: true
        },
        {
          username: 'Laura',
          online: true
        }
      ]
    }
  }
  render() {
    const usersOnline = this.state.users.filter(user => user.online); // change code here
    const renderOnline = usersOnline.map(x => <li key={x.username}>{x.username}</li>); // change code here
    return (
       <div>
         <h1>Current Online Users:</h1>
         <ul>
           {renderOnline}
         </ul>
       </div>
    );
  }
};



//Render React on the Server with renderToString
class App extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <div/>
  }
};
// change code below this line
ReactDOMServer.renderToString(<App />);
```

This was a VERY hard challenge, instructions were not very clear and for the most part examples were non existent.

**Link(s) to work**

1. Finished work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedChange Inline CSS Conditionally Based on Component State
* PassedUse Array.map() to Dynamically Render Elements
* PassedGive Sibling Elements a Unique Key Attribute
* PassedUse Array.filter() to Dynamically Filter an Array
* PassedRender React on the Server with renderToString

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).
