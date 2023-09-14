# Redux 

*is an open-source JavaScript library for managing the state of a web application. It is commonly used in conjunction with React, although it can be used with other libraries and frameworks as well. Redux provides a predictable and centralized way to manage and update the state of an application, making it particularly useful for building complex and data-driven web applications.*

## What is the first principle of Redux?

The first principle of Redux is **"Single Source of Truth."** It means that the entire state of your application is stored in a single JavaScript object called the **"store."** This ensures that there is one central place to access and modify the state, making it predictable and easier to manage.

## What is a store and what do we use our reducers for within that store?

A store in Redux is a JavaScript object that holds the application's entire state tree. It is the core of Redux and provides methods for interacting with the state. Reducers in Redux are functions responsible for specifying how the application's state changes in response to actions. They take the current state and an action as input and return a new state. Reducers are used within the store to update the state in a predictable and controlled manner.

## Redux store methods given to us by createStore and describe their use.

1. getState(): 
    * This method is used to retrieve the current state stored in the Redux store. It returns the current state object, allowing you to access and display the state data in your application's UI.

2. dispatch(action): 
    * The dispatch method is used to dispatch actions to the Redux store. Actions are plain JavaScript objects that describe the type of operation or change that needs to be made to the state. Dispatching an action triggers the appropriate reducer functions, which update the state accordingly.

3. subscribe(listener): 
    * subscribe is used to add a callback function (listener) that will be invoked whenever the state in the Redux store changes. It allows your application to react to state changes and update the UI accordingly.

## what combineReducers() does and why it is useful.

**combineReducers()** is a utility function provided by Redux that is used to combine multiple reducer functions into a single reducer. It is useful because, in a large Redux application, you often have multiple pieces of state to manage, each with its own reducer function. combineReducers() allows you to create a single reducer function that orchestrates the state updates for all these individual pieces of state.

Imagine your application has different parts of the state, such as user data, product information, and notifications. Each of these parts can have its own reducer function. combineReducers() helps organize these reducers by letting you create a root reducer that delegates the responsibility of each part's state to its respective reducer. This makes the codebase more modular, maintainable, and easier to reason about, as each reducer focuses on a specific part of the state. It also simplifies the process of updating and managing the overall application state.