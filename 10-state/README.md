# State management - front-end web technology

Keep state, react on changes, efficiently!

Please read:

- [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)
- [Passing Data Deeply with Context](https://react.dev/learn/passing-data-deeply-with-context)
- [Scaling Up with Reducer and Context](https://react.dev/learn/scaling-up-with-reducer-and-context)
- [Reusing Logic with Custom Hooks](https://react.dev/learn/reusing-logic-with-custom-hooks)

## Why is state management exciting?

- State is what makes front-end harder than back-end development
  - Scalable to large and complex data structures
  - Reactive to any change
  - Synchronization with other state representations
  - Performance
  - Developer experience

## Where can state be kept?

- **Component** - with React `useState` and `props`
  - Too much code repetition
- **Local storage** - with `localStorage` Web API
  - Reactivity must be handled manually
- **URL** - in query or hash part
  - URL has a length limit
  - Privacy issue when sharing
- **global variables**
  - Reactivity must be handled manually
- **React Context** - less repetition
- **Redux** and other libraries - selectors for performance
- **Server** - persistant across sessions
  - Reactivity must be handled manually

For a somewhat serious example of storing state in the URL, look at this cute little world-builder game demo: https://oskarstalberg.com/Townscaper

## What's wrong with useState and props?

- Passing state up and down the component hierachy is a very verbose
- Refactoring component structure becomes very tedious
- Refactoring state structure becomes very tedious

## useReducer - reactive objects

- Combining a set of properties into a single state
- Transactionally update set of properties
- Works like a state machine
- Must be pure - no side-effects
- Immutable to support reactivity

## React Context

How it works:

- First: _provide_ the context at the top
- Second: _use_ the context at any deeper level without passing through props
- Separate into multiple contexts for improved reactive performance
- Separate into state and dispatch contexts for improved reactive performance

Example code structure:

```tsx
// Type of state
type MyState = {...}

// Initial state
const initialMyState = {...}

// Type of actions
type MyAction = { type: 'do-this', payload: {...} } | ...

// Reducer
const myReducer = (state, action) => { switch(action.type) { case 'do-this': return ... } }

// State context
const MyContext = createContext<MyState | null>(null)

// Dispatch context
const MyDispatchContext = createContext<React.Dispatch<MyAction> | null>(null)

// Provider
type MyProviderProps = React.PropsWithChildren<{myState?: MyState}>
function MyProvider({ children, myState: explicitMyState }: MyProviderProps) {
  const [myState, myDispatch] = useReducer(myReducer, explicitMyState || initialMyState);
  return (
    <MyContext.Provider value={myState}>
      <MyDispatchContext.Provider value={myDispatch}>
        {children}
      </MyDispatchContext.Provider>
    </MyContext.Provider>
  );
}

// state hook
function useMyState() {
  const myState = useContext(MyContext);
  if (myState === null) {
    throw new Error("Unexpected useMyState without parent <MyProvider>");
  }
  return myState;
}

// dispatch hook
function useMyDispatch() {
  const dispatch = useContext(MyDispatchContext);
  if (dispatch === null) {
    throw new Error(
      "Unexpected useMyDispatch without parent <MyProvider>"
    );
  }
  return dispatch;
}
```

## Typing for context

- add `| null` to the type and throw if null in `useMyContext`

## Testing context with explicit initial state

- Pass in optional explicit initial state
- Provide explicit initial state in tests

## Clean code

- Extract state into contexts
- Extract into smaller components becomes easier with context
- Extract hooks to combine values from different context
- Extract non-react functionality into plain functions for easier testing

## Next time

[Security](../11-security/).
