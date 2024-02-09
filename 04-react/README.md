# React - front-end web technology

The most popular UI framework.

Please read:

- [Quick Start](https://react.dev/learn) from Facebook.
- [Thinking in React](https://react.dev/learn/thinking-in-react) from Facebook.
- [Describing the UI](https://react.dev/learn/describing-the-ui) from Facebook.
- [Adding Interactivity](https://react.dev/learn/adding-interactivity) from Facebook.
- [Using TypeScript](https://react.dev/learn/typescript) from Facebook.

## Supplemental reading material

- [Tutorial: Tic-Tac-Toe](https://react.dev/learn/tutorial-tic-tac-toe) from Facebook.

## Why is React exciting?

- React is the most widely used and highly liked UI framework:
  - https://2022.stateofjs.com/en-US/libraries/front-end-frameworks/
- React is in active development with a friendly community
- As a library, React composes well with other technologies
- React scheduling easier (for me) to reason about than event streams and signals

## Components

- A component is a top-level function that returns a React element
- Keep components pure:
  - only change local variables
  - same output for same input
- Nest components
- JSX: syntax to create React elements
  - shorthand for `React.createElement()`
  - `className` (instead of HTML `class` attribute)
  - Embed JavaScript between `{` and `}`
- Conditional rendering
- Iterated rendering with the `key` attribute
- Attaching event handlers

## State

- useState
- subscription: trigger re-rendering when state changes
- state doesn't actually change until next re-render
- Use object/array spread operator `...` to change state partially

## Props

- A parent component can pass props to a child component
- Keep state in high level components, but not higher than needed
- Pass state down to sub-components as props, to read state
- Pass state change handler down to sub-components, to change state
- Child elements as props

## Rendering

- In React, rendering means calling components to produce React elements
- State updates request a re-render of component and children
- After rendering, React will commit only the changed elements to the DOM
- Browser will then paint those changes in the DOM

## React Diagram

- https://github.com/larsthorup/react-diagram

## React Dev Tools

- https://react.dev/learn/react-developer-tools

## Next time

[Testing](../05-testing/).
