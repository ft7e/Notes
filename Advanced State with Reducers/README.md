# Advanced State with Reducers

## What is useReducer?

An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method.source (Links to an external site.)

useReducer is a built in Hook in React is used to state management in React. useReducer is an alternative to useState. It is related to reducer functions.

## Why we use useReducer over useState?

useState is used, when state values are primitives, state values are only used in a single component inside or logic is simple.

useReducer is used, when we have complex state like involves objects or arrays, next state is depend on previous one, data share among the components and update state more complex. useReducer is optimized performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
