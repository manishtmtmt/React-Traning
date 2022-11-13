## 1. If you need a protected page and you use React Router, how would you approach it?

**Ans:** _I would create a custom component and based on some condition would allow route to render_

With React Router, in order to implement private/public routes you need to create a custom component, a wrapper around `<Route />` with custom logic. Based on the logic, you would either render the route or display access denied or maybe even redirect user to other route.

## 2. What type of a database firebase has?

**Ans:** _NoSQL (json-based)_

Firebase has 2 databases to your disposal: firestore and real-time database. Both are NoSQL databases.

## 3. How you can redirect user to another page with React Router?

**Ans:** _Use `<Redirect />` component from React Router or by using React Router hooks_

React Router has Redirect component and useHistory hook that gives more granular control over browser's History API (push/replace route)

## 4. What is a UI-components library?

**Ans:** _A library with a set of predefined components that can be used in the app_

A UI-component library is a set of predefined reusable components that can be used in the app in order to save time creating similar components ourselves (e.g., Drawer, Modal, Slideshow)

## 5. What's the point of Context API?

**Ans:** _To pass some value down the component tree without using "intermediary" components_

Context API allows to pass some context(value) to component's deeply nested children without the need to use "intermediary" components. This eliminates the problem of prop drilling.

## 6. Name the hook that allow to access context value

**Ans:** _useContext_

The useContext() hook can be used to access the context value. When useContext() is called, as an argument you must pass the context you want to access.
