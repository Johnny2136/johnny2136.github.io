---
layout: post
title: Day 42 of 100 Days Of Code
---

![Image from React and Redux](http://onsen.io.s3-website-us-east-1.amazonaws.com/blog/content/images/2016/Jun/react_redux.png)

## Day 42: September 4, Tuesday

**Today 's Progress**: I finished work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Done with Redux and will start React and Redux tomorrow misleading instructions and no relevant examples these challenges are NOT a good way to learn these two frameworks.

### Resources used:
  * [Using Object Spread Operator](https://redux.js.org/recipes/usingobjectspreadoperator),
  * [Is this the correct way to delete an item using redux?](hhttps://stackoverflow.com/questions/34582678/is-this-the-correct-way-to-delete-an-item-using-redux)

  ## Remove an Item from an Array
  Instructions sucked and an example would have been nice...
  Finish writing the reducer so a new state array is returned with the item at the specific index removed.
  ```Redux
  const immutableReducer = (state = [0,1,2,3,4,5], action) => {
    switch(action.type) {
      case 'REMOVE_ITEM':
        // don't mutate state here or the tests will fail
        let newArr = [...state.filter((elem, idx) => { // [1,2,3,5]
          return idx !== action.index
        })];
        return newArr;
      default:
        return state;
    }
  };
  const removeItem = (index) => {
    return {
      type: 'REMOVE_ITEM',
      index
    }
  };
  const store = Redux.createStore(immutableReducer);
  ```

  ## Copy an Object with Object.assign
  Edit the code to return a new state object for actions with type ONLINE, which set the status property to the string online. Try to use Object.assign() to complete the challenge.
  ```Redux
  const defaultState = {
    user: 'CamperBot',
    status: 'offline',
    friends: '732,982',
    community: 'freeCodeCamp'
  };
  const immutableReducer = (state = defaultState, action) => {
    switch(action.type) {
      case 'ONLINE':
        // don't mutate state here or the tests will fail
        const newObject = Object.assign({}, state, {status:'online'})
        return newObject;
      default:
        return state;
    }
  };
  const wakeUp = () => {
    return {
      type: 'ONLINE'
    }
  };
  const store = Redux.createStore(immutableReducer);
  ```
**Link(s) to work**

1. Finished work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedRemove an Item from an Array
* PassedCopy an Object with Object.assign

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).
