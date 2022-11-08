## 1. A component is basically ...

**Ans:** *A function or a class*

**Explanation:** Component can only be either a function or a class.

## 2. What's the name of React's mixed HTML and JavaScript syntax?

**Ans:** *JSX*

**Explanation:** React has it's own syntax - JSX - that gets complied back to JavaScript. It resembles HTML but in reality it's JavaScript. Worth to mention that in old versions of React, there was no JSX and components were written in pure JavaScript.

## 3. What are component properties?

**Ans:** *Props are custom, user-defined component attributes. They can be defined on any component, can have any name and pass any value*

**Explanation:** Component props are custom attributes that can be passed to a component and accessed inside the component. They look like html attributes, but they are custom-defined.

## 4. What will happen if you put some value inside a variable instead of state.

**Ans:** *The value inside a variable will not be persisted across component re-renders since every React re-render is unique and not aware of the other ones*

**Explanation:** If you would use a variable as a replacement for state, on every subsequent re-render variable's value will stay the same. Every render is isolated and not aware of other renders. On every re-render, React will create a new copy a variable thus the value will not persist.

## 5. What React hooks allow us to do?

**Ans:** *They allow to manipulate the state and hook into lifecycle events*

**Explanation:** React hooks allow to 'hook' into component lifecycle events and state management. Custom hooks allow to reuse stateful logic multiple times across multiple components. React hooks are meant to replace class-based components.

## 6. When a components renders on the page, what lifecycle event is triggered?

**Ans:** *ComponentDidMount*

**Explanation:** A component mounts/renders on the page, that's why componentDidMount is fired only once when component is rendered.