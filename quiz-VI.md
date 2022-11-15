## 1. How can you specify what place to update in firebase real-time database using firebase-sdk?

**Ans:** *I must specify database place as a path-string: /path/to/some/place/*

To update firebase realtime database you must specify database path in form of /path/to/some/place. Because the database is JSON-based it's roughly equivalent how you access javascript object keys.

## 2. Choose the most correct statement for React references (useRef)

**Ans:** *One use-case for references is to 'reference' HTML elements. It will allow to directly manipulate the referenced HTML element and access its DOM properties*

React references should be used when you deal with HTML elements or non-standard objects from different libraries. You should remember that almost always you want to use state (state and references are completely different and not related to each other). The most common use-case is to create a reference for an HTML element in order to directly manipulate the element and its DOM properties (e.g., scrollTop)

## 3. How you specify default props in a function component?

**Ans:** *In the same way as for default function arguments*

Component is eventually just a function and props are basically functions arguments. You would specify default props in the same manner as for regular functions.

## 4. How you can pass multiple properties to a component at once?

**Ans:** *Use the spread operator to spread an object of props over the component. `<Comp {...props} />`*

The spread operator can be used to spread an object over a component. Props are just an object where keys are prop names. `<Component {...allProps} />`

## 5. How to get current pathname using React Router?

**Ans:** *Must call the useLocation hook and get pathname from the returned object*

You can use useLocation hook. This hook returns an object with information about current browser location. Inside returned object you can find pathname.

## 6. What are security rules in firebase?

**Ans:** *Security rules define read/write/delete access permission to database locations and storage objects*

Security rules define access to realtime database/firebase/storage. All firebase services can be accessed via publicly available URL (including database and storage). If security rules are not established correctly, a malicious user can easily manipulate database/storage data using the public url. You can customize security behaviour for every path and for every object inside the database/storage.