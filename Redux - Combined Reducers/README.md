# Redux - Combined Reducer

## Why create multiple reducers?

Multiple reducers are created to manage different parts of the application state separately. In a complex Redux application, it is often necessary to break down the state management into smaller, more manageable pieces. Each reducer is responsible for handling a specific part of the application's state, making the codebase more modular and maintainable.

## How would you combine multiple reducers?

You can combine multiple reducers using the combineReducers utility provided by Redux. This function takes an object where each key represents a slice of the state and each value is a reducer function responsible for managing that specific slice. It returns a single reducer that can be used to create the application's state tree.

## How will you manage state as an immutable object? why?

Redux encourages managing state as an immutable object to ensure predictability and ease of debugging. When state is immutable, it becomes easier to track changes, as you can be sure that any modifications to the state result in a new state object, rather than modifying the existing one. This immutability helps with debugging, time-travel debugging, and avoiding unintended side effects.

# Redux Docs: Using Combined Reducers

combineReducers is a utility function to simplify the most common use case when writing Redux reducers.
The missing word here is "Redux reducers." combineReducers simplifies the process of combining multiple reducers into one reducer function.

## How combineReducers assembles the new state tree.

combineReducers assembles the new state tree by taking an object where each key represents a slice of the state and each value is a reducer function responsible for managing that slice. When an action is dispatched, combineReducers calls each individual reducer with the corresponding slice of the state, and then it combines the results into a single state tree.

## How would you define initial state in an app using combineReducers?

You can define the initial state for an app using combineReducers by providing an initial state object as the second argument to combineReducers. This initial state object should have the same structure as the state slices managed by the individual reducers.

# Redux Docs: Combined Reducer Syntax

## Why will you want to split your reducing functions as your app becomes more complex?

You will want to split your reducing functions as your app becomes more complex to maintain a clear and organized code structure. Splitting reducers allows you to focus on specific parts of the state and their corresponding logic, making it easier to debug, test, and scale your application.

The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.
The missing word here is "createStore." The combineReducers function combines multiple reducers into a single reducer that can be passed to the createStore function to create the Redux store.

## What is a popular convention when naming reducers?

A popular convention when naming reducers is to use descriptive names that indicate the slice of state they manage. For example, if you have a reducer responsible for managing the state of user data, you might name it userReducer. This naming convention helps developers quickly understand the purpose of each reducer in a large application.