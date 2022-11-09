## 1. If you render null, what will be displayed?

**Ans:** *Nothing will be rendered*

In React, if you try to render "falsy" values they will be literally considered as nothing and ultimately nothing will be rendered. If you need to render falsy values, consider converting them to a string (i.e., null => "null")

## 2. Why do we need React router?

**Ans:** *To create multiple pages/routes in a SPA*

React router allows to create multiple pages/routes in Single Page Apps. It manipulates the browser's History API and is client-side only, means that it is fully powered by JavaScript.

## 3. What will you use to call an API from a browser?

**Ans:** *fetch*

To send an http request, you must use browser's fetch.

## 4. Where API result must be stored after you have it?

**Ans:** *In state (e.g., useState)*

Data that changes (not computed values) must reside inside state as otherwise, it won't persist across component re-renders.

## 5. What problem does Styled-components solve?

**Ans:** *SC create component-scoped styles. This solves the problem of globally scoped css styles.*

When using normal CSS files, all styles/classes are shared in the global scope. It means that efvery classname must be unique to avoid conflicts. This is not very convenient. Styled components create component-scoped styles and ensure that if you create 2 different components with same styles, they will have no conflicts.

## 6. Can you style already existing components with Styled-components?

**Ans:** *Yes, you can extended styles of any existing component.*

SC allows to style/extend styles of any existing component, whether it was created by user or a component comes from a library.