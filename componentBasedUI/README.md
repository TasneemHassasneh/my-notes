# Component Based UI

1. Building blocks of a React app:
    The building blocks of a React app are components. Components are the individual units that encapsulate a part of the user interface and its behavior. React apps are built by composing these components together to create complex UIs.

2. Difference between an HTML element and a React component:
    An HTML element represents a single element in the DOM (Document Object Model) and is part of the web's native structure. In contrast, a React component is a JavaScript function or class that defines a reusable piece of UI with its own logic, state, and props. React components can render HTML elements, but they can also manage their own internal state and behavior.

3. JSX and its usage:
    JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code within your JavaScript code. It's used in React to define the structure of UI components in a more declarative and readable manner. JSX gets transpiled into regular JavaScript function calls by tools like Babel, making it possible for React to understand and render the components.

4. Embedding JavaScript expressions in JSX:
You can embed JavaScript expressions within JSX by wrapping them in curly braces {}. For example, if you want to display a variable's value, you can do so like this: {variableName}.

5. React and JSX features for iteration or conditional logic:
    React provides map functions and conditional rendering to handle iteration and conditional logic. JSX allows you to use JavaScript expressions directly within the markup to achieve conditional rendering and dynamic content generation.

6. How React responds to user inputs:
    React responds to user inputs by updating its components' state and re-rendering those components as necessary. When a component's state changes, React automatically updates the DOM to reflect the changes.

7. Word indicating a React component uses a Hook to manage data:
    The word is "useState" which refers to the state hook in React. A component that manages data using the useState hook is utilizing React's built-in state management system.

8. Sharing data between React components:
    Data sharing between React components can be achieved by passing data through props (properties) or using a state management solution like React Context or a third-party state management library like Redux.

## Render and Commit

*Three steps of refreshing a React UI: The three steps of refreshing a React UI are:*

1. Re-rendering:
React updates the virtual DOM to reflect changes in the component's state or props.

        **Diffing:** React compares the updated virtual DOM with the previous virtual DOM to identify the minimal set of changes needed.

        **Updating:** React applies these changes to the actual DOM, ensuring that the user interface reflects the updated component state.

        **Triggering updates to a component after initial render:** Updates to a component after the initial render can be triggered by changing the component's state using setState (or useState hook) or by receiving new props from a parent component.

2. Recreating DOM nodes on every rerender:
    No, React doesn't recreate all DOM nodes on every re-render. Instead, it performs a process called "reconciliation," where it identifies the differences between the previous and current virtual DOM trees and applies only the necessary changes to the actual DOM.

3. Final step before the user sees DOM changes after React update:
    After React has updated the DOM, the browser needs to repaint and reflow the page layout to reflect the changes visually. This step is known as the "layout and paint" phase and is performed by the browser's rendering engine.
