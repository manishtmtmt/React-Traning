## 1. How loading spinner can be implemented?

**Ans:** *Create a state with boolean value and based on the value render the spinner*

You create a simple boolean state that will indicate whether data is loading or not. You would update the state to true/false when you receive data (e.g., from an API).

## 2. What React hook can we use to execute some logic only once when component mounts?

**Ans:** *useEffect*

useEffect allows to manipulate componentDidMount, componentDidUpdate and componentWillUnmount lifecycle events. If useEffect hook has empty dependency array, the effect will run only once.

## 3. What is a custom hook?

**Ans:** *A function that allows to create reusable logic with built-in react hooks*

Custom hook is a function outside of a component that extracts reusable logic written with built-in React hooks. Custom hooks can be used only inside components.

## 4. What does it mean when prop name is just passed to the component without any value? `<Component someProp />`

**Ans:** *Prop is considered to be true (boolean)*

When prop is passed without any value, just prop name, React considers this prop to be true (boolean).

## 5. Is there any limitations on custom hooks (i.e., number of created hooks)?

**Ans:** *No, there is zero limitations on custom hooks in particular. It has same rules as normal built-in React hooks.*

Custom hook is a reusable function with built-in React hooks. It does not have any limitations. It has the same rules/guidelines as built-in react hooks.

## 6. Main difference between useReducer and useState?

**Ans:** *useReducer uses reducer, actions and dispatch while useState does not have it all*

useReducer takes different approach to state management by utilizing reducers, actions and dispatch. useState gives simple and primitive way to update the state by just passing the new value.