## 1. Name three main components of the reducers pattern?

**Ans:** _Reduccer, Dispatch, Action_

Three main keywords of the reducer pattern are 1) Action; 2) Dispatch; 3) Reducer itself

## 2. What naming convention all custom hooks must have?

**Ans:** _Hook name must be prefixed with "use"_

The convention for all hooks (incl. custom and built-in) is that hook name must be prefixed with "use". Example are useState, useEffect, useCustomName

## 3. When to use the useCallback hook?

**Ans:** _When we need to inform React that new function copy should NOT be created on every re-render_

useCallback is used to optimize functions inside components. It preventss creating a new copy of the function on every re-render. useCallback should NOT be used all the time.

## 4. What useEffect can do?

**Ans:** _useEffect allows to "hook" into the next lifecycle events: componentDidMount, componentDidUpdate, componentWillUnmount and run the effect (callback function)_

useEffect allows to "hook" into the next lifecycle events: componentDidMount, componentDidUpdate, componentWillUnmount. It runs an effect (callback function) when one of the lifecycle methods is triggered. The cleanup function of useEffect can hook into componentWillUnmount

## 5. How can you tell React Router that you need a dynamic route?

**Ans:** _Must specify a dynamic key in the "path" prop of Route: `<Route path="/some/page/:key" />`_

You must specify a dynamic key in the "path" prop of Route: `<Route path="/some/page/:key" />`. Then the key can be retrieved inside the underlying components and used to fetch dynamic data.

## 6. Name three lifecycle events that useEffect allow us to "hook into"?

**Ans:** _componentDidMount, componentDidUpdate, componentWillUnmount_

Every React component goes through three main lifecycle events: componentDidMount, componentDidUpdate, componentWillUnmount. useEffect can trigger the effect (callback) on each.

## 7. How can you apply dynamic styles to Styled-components?

**Ans:** _Using string interpolation, JavaScript logic can be placed inside CSS markup. Inside this logic you have access to custom props passed to the component._

## 8. Why children of a component do re-render even though they don't need to?

**Ans:** _Because React is designed this way. Data always flows from top to bottom (from parents to children)._

React's is designed is in a way that children of a component will rerender when the component updates/rerenders. This is because of Flux - React's architectural design that defines how data flows: from top to bottom.

## 9. What is an array of dependencies in useEffect/useCallback?

**Ans:** _Array of dependecies tells React when to rerun/update the hook_

Array of dependencies in useEffect and useCallback tells React when to update the value passed to the hook. In case of useEffect, if one the elements in array of dependencies changes, the "effect" will re-run. In case of useCallback, a new copy of the function will be created.

## 10. What is a custom hook?

**Ans:** _A function that allows to create reusable logic with built-in react hooks_

Custom hook is a function outside of a component that extracts reusable logic for built-in React hooks.

## 11. What is Flux?

**Ans:** _Flux is a pattern that defines how data flows in React: from top to bottom (from parents to children)_

Flux is a pattern for managing how data flows through a React application. This is the architectural design behind React.

## 12. How would you solve "Can't perform a React state update on an unmounted component"?

**Ans:** _Create a boolean variable inside useEffect (e.g., isMounted) or a boolean state if not using useEffect. The boolean will indicate whether the component is currently rendered. Then right before updating the state check against the boolean._

The only way to deal with this is to check whether component is currently rendered on the page by using either a boolean vaiable inside useEffect or by creatin boolean state. Then before updating the state, you would check if component is current mounted, if yes - perform the logic, if no - don't update the state.

## 13. When you would use browser's local storage?

**Ans:** _When I need to persist some data when the page refreshes or when the browser is closed_

Local storage and session storage are browser's APIs that can used by client-side JavaScript. They allow to store some information directly inside the browser storage. This is useful when some data must be persisted over page refreshes or when user closes the browser (e.g., user theme preference or last input state). Local storage is vulnerable to scripting attacks. For that reason it should not store any sensitive information.

## 14. Tell the difference between local and session storage

**Ans:** _Local storage persists data even if tab or browser is closed. Session storage stores data only for "current user session" and will be cleared as soon as user closes the current tab_

Local storage persists data even if tab or browser is closed. Session storage stores data only for "current user session" and will be cleared as soon as user closes the current tab

## 15. What is the reducer function?

**Ans:** _A function that computes and produces new state_

The reducer function is a function that process data sent by the dispatcher (dispatch). It 'reduces' multiple inputs and produces new state. Every useReducer hook expects a reducer as one of the arguments.

## 16. Why memo() won't work on a component that receives Object/Function as one of the props?

**Ans:** _Because memo() does strict and shallow comparison of previous and new props. If objects/functions are referentially changed, memo() will fail to compare them_

memo() compares previous and new component props. If they are different, it updates the component. For comparison it uses 'strict' equality (===). If 2 objects are compared (that look the same) and these objects point to different place in memory, React will consider that they are different.

## 17. What will happen if you leave an empty array of dependencies for useEffect even though the hook has a few dependencies?

**Ans:** _useEffect will run only once when the component mounts. Even if the state will change in the future, the useEffect hook will not rerun the effect_

If useEffect has an empty array of dependencies, the effect will run only once when the component mounts. If useEffect uses a state that changes and the state is not listed in the array of dependencies, useEffect will still run only once when the component mounts and future state updates will not affect the useEffect hook.

## 18. What technique can be used to prevent child component from rerendering?

**Ans:** _memo()_

## 19. Choose the most appropirate elements that characterize PWA (Progressive Web App)

**Ans:** _service worker, manifest file, https_

PWA can be characterized by 3 elements: 1) manifest file (describes the app such as name, icons and colors); 2) https (every PWA requires secure connection); 3) service worker (a script inside browser that handles efficient caching of the resources).

## 20. What are the benefits of PWA (Progressive Web App)?

**Ans:** _The app loads faster because of service worker caching and it can even work offline. Can be installed as a native app_
