---
title: Use a Switch Statement to Handle Multiple Actions
---
## Use a Switch Statement to Handle Multiple Actions

Tip: Make sure you don't use "break" commands after return statements within the switch cases.


const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  // change code below this line
  const typeOfActiction = action.type;
  switch (typeOfActiction) {
    case 'LOGIN':
     return  {authenticated: true}
    case 'LOGOUT':
      return {authenticated: false}
    default:
  return defaultState;

  }
  // change code above this line
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: 'LOGIN'
  }
};

const logoutUser = () => {
  return {
    type: 'LOGOUT'
  }
};
