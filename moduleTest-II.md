 ## 1. What does Parcel do?

 **Ans:** *Parcel is a tool for bundling the project with zero config*

 Parcel is a tool for bundling the project with zero config. It can automatically compile/transpile and execute JavaScript/CSS/HTML. Other cool things such as minifaction are also included.

 ## 2. What will happen if you put some value inside a variable instead of state.

 **Ans:** *The value inside a variable will not be presisted across component re-renders since every React re-render is unique and not aware of the other ones*

 If you would use a variable as a replacement for state, on every subsequent re-render variable's value will stay the same. Every render is isolated and not aware of other renders. On every re-render, React will create a new copy a variable thus the value will not persist.

 ## 3. What is <>...</>?

 **Ans:** *It's React Fragment (empty element). Can be used to wrap HTML markup to produce a single element*

 `<>...</>` is React Fragment and it represent an empty element/component.
 `<>...</>` is shorthand for `<React.Fragment>...</React.Fragment>`

 ## 4. What useState hook returns?

 **Ans:** *An array of exactly 2 elements: state value and an update function that must be called to update the state*

 The useState hook returns an array of exactly 2 elements: state variable and an update function that must be called to update the state

 ## 5. What is React's mounting point?

 **Ans:** *A container for React application (HTML element)*

 React's mounting point is an HTML element (usually `<div id="root" />`) that will be used as a container for React application. React component tree will be insterted inside the mounting point.

 ## 6. If one would ask you: "How to manage styles in React app?". How would you answer the question?

 **Ans:** *Any approach that is commonly accepted (e.g., inline-styles, SASS, etc.)*

 A React app can be styled in literally any way: from inline CSS to CSS-IN-JS solutions (e.g., styled-components)

 ## 7. What is conditional rendering?

 **Ans:** *Conditionaly render markup based on some condition*

 Conditional rendering is pretty self-explanatory: it means that something (i.e., markup) will be renderend based on some condition. For example, render an array of elements if array is not empty.

 ## 8. What events can we bind to an html element in React?

 **Ans:** *React can handle all events that exist on real HTML element in real DOM (e.g., onClick, onChange, etc.)*

 React supports binding for all elements events that are supported by real HTML elements (e.g., onClick, onMouseOver, etc).

 ## 9. What is a children prop?

 **Ans:** *The children prop refers to markup passed to a component like that: `<Component>This is children</Component>`. Can be accessed inside Component via props.children*

 The children prop refers to markup passed to a component like that: `<Component>This is children</Component>`. Inside Component children can be accessed via props.children

 ## 10. If a component is re-rendered, what happens to all elements/components inside the component?

 **Ans:** *All inner and nested elements/components will be re-rendered too*

 When a component is re-rendered, all children and nested elements are re-rendered too. If a component has nested components, they will re-render as well unless manually optimized.

 ## 11. When we map array values to JSX markup, what prop we must pass to the mapped element?

 **Ans:** *The "key" prop `<Elem key={val} />`*

 The "key" props must be passed to a mapped JSX element. Key must be unique. It is not acceptable in React that 2 elements have the same key. For dynamic arrays that change frequently, you should use unique id generator. For arrays that do not change frequently, passing element index is sufficient.

 ## 12. What does ReactDOM.render(...) do?

 **Ans:** *Mounts react application onto the webpage using React's mounting point. Must be called once to render the application*

 ReactDOM.render mounts React's component tree onto the webpage using provided mounting HTML element.

 ## 13. What are three main methods of component's lifecycle?

 **Ans:** *componentDidMount, componentDidUpdate, componentWillUnmount*

 Every React component goes through three main lifecycle events: mount, update, unmount. So every component can access each of the events by using one of the methods respectively: componentDidMount, componentDidUpdate, componentWillUnmount.

 ## 14. How many different types of arguments (overloads) we can pass to useState's update function?

 **Ans:** *2*

 useState's update function supports only 2 type of arguments (2 overload available):
 - pass new value that will replace current state
 - pass a callback function that receives current state as an argument. It must return some value that will replace current state. Useful when previous state must be accessed to compute next state.

 ## 15. Why would you ever lift up the state to parent component?

 **Ans:** *To share the state between multiple children components*

 You would lift up the state when it must be shared accross multiple components. You define the state in parent component and pass the state via props to children components.

 ## 16. What is "style" prop on html elements in React?

 **Ans:** *The "style" prop is used to set element's inline styles*

 The "style" prop is intended for element inline styles. Since in React we operate with JavaScript, the style prop must be an object where keys are camelCased css properties.

 ## 17. If a prop is expected inside a component but it is not being passed, what value will the prop have?

 **Ans:** *undefined*

 The prop will be set to undefined. Props work very similary to function arguments.

 ## 18. How to apply dynamic classes to an element?

 **Ans:** *Use one of these to update the "className" prop: string interpolation, ternary operator (? :), a function that returns new string on every re-render*

 Pass the 'className' prop which is string to the element. The string can be manipulated with JavaScript and changed dynamic inside the component. The most common way to do that is to use string interpolation.

 ## 19. What happens under the hood when we run the build command? (i.e., npm run build)

 **Ans:** *A prodect manager (module bundler) will process all the source code and produce a production version that is optimized and can used for deployment*

 Project builder/manager will bundle all source code to the production version. Here are a few operation that can potentially take place:
 - Source code is minified
 - Source code is processed/transpiled
 - Source code is optimized
 - Unused source code is removed (dead code elimination)

 ## 20. Choose the correct statement

 **Ans:** *A component must always return a single element*

 A component must always return a single element. That's the golden rule of React components. Otherwise, React will produce an error.

 ## 21. Imagine you have a component that is being used 3 times. Inside the component you wrote console.log("hello") 2 times. When the component mounts, how many console.logs you will see in browser's console?

 **Ans:** *6*

 Inside a component you have two console.log('hello') statements, so when the component renders you will see 2 console logs in browser's console.
 When the component renders 3 times, for each render you will have 2 console logs, meaning 3 * 2 = 6.