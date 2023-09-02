# Context API

## Choosing the State Structure

*The five principles for structuring state are as follows:*

1. **Group related state:**

    Combine state variables that always update together into a single state variable to ensure they stay in sync.

2. **Avoid contradictions in state:** 

    Organize state in a way that prevents conflicting or contradictory states. For example, use a single status state variable instead of separate variables that can be in conflicting states.

3. **Avoid redundant state:** 
    
    Don't store information in state that can be derived from existing props or other state variables during rendering. This reduces unnecessary duplication of data.

4. **Avoid duplication in state:** 
    
    When the same data is duplicated between multiple state variables or nested objects, it becomes challenging to keep them synchronized. Reduce duplication by structuring state efficiently.

5. **Avoid deeply nested state:** 

    Deeply hierarchical state can be difficult to update and manage. Flatten state when possible to make it easier to work with and reduce the chances of introducing bugs.

## Passing State Deeply with Context

Context in React aims to solve the problem of passing data from a parent component to deeply nested child components without having to pass the data explicitly through each intermediate component using props. It allows a parent component to make information available to any component in the tree below it, no matter how deep, without the need for **"prop drilling."**

Before using useContext, one technique to try is passing props explicitly through the component tree. This is the traditional way of passing data down to child components using props.

For complex applications, useReducer is a hook that complements useContext when managing state within a context. It allows you to handle more complex state management scenarios, especially when multiple components need to modify and interact with the same piece of shared state.