## 1. What's the good place for a subscription (real-time listener)?

**Ans:** *useEffect*

useEffect is a good place for a subscription because you want to subscribe to data changes when the component mounts and unsubscribe when the component unmounts. useEffect allows you to do so.

## 2. Name two main elements of Context API

**Ans:** *Provider and Consumer*

Context API consists of Provider (a component that provides the context value) and Consumer (a component that gets the context value)

## 3. Where you would unsubscribe from a subscription in useEffect?

**Ans:** *In the cleanup function*

Subscriptions (real-time-listeners) must be canceled in the cleanup function inside useEffect

## 4. How can you get url parameters (if there is any) in a component if you have React Router in your app?

**Ans:** *Must use useParams hook from react-router*

You can get use of React-Hooks that come from the react-router package. useParams can retrieve and parse url parameters

## 5. What is prop drilling?

**Ans:** *Passing props on many levels down the component tree*

Term "prop drilling" refers to a situation where you pass props down the component tree many levels deep.

## 6. What problem does Context API solve?

**Ans:** *Prop drilling (no intermediary components)*

Context API solves the problem of prop drilling by allowing to pass some value down the component tree on many levels deep without using intermediary components.

## 7. How will you access current value of a reference in React?

**Ans:** *muRef.current*

You can access current value of a reference by accessing .current key of the reference -> myRef.current; You can put anything you want in a reference but you should prefer state whenever is possible.

## 8. What is the downside of Context API?

**Ans:** *Context API doesn't have partial selection of the context value. Must split large object into multiple contexts.*

Context API doesn't have partial selection of context value. It means that passing an object to context will always result in a rerender even tough you want to only select one key from  the object. This can be solved by splitting every object key into its own context.

## 9. Why to denormalize (copy data) in a NoSQL database?

**Ans:** *To prevent multiple database queries and optimize read performance*

Since there is no SQL-like joins available in NoSQL databases, data denormalization is the moset efficient approach to prevent sending multiple queries to the database. Related data is groupted and stored together. It's like storing SQL-join results upfront. Imagine a book record. Every book is associated with an author. Normally, you want to store author id next to book data, however if you want to display author data next to the book, knowing only author ID you can't do the because there is no SQL-lik joins in NoSQL world. You need to send another request to get author profile data. To avoid this kind of situations, instead of author ID, you would store author data that you want to display.

## 10. What is the main disadvantage of data denormalization in NoSQL database?

**Ans:** *Data is duplicated and all duplicated references must be manually updated when the original updates*

The bad thing about data denormalization is you actually need to copy/duplicate data. This becomes harder to manage compared to SQL databases. 1) You need to know what shape of data to denormalize; 2) You must manually updates all duplicates; 3) It becomes harder to manage when data structure becomes more sophisticated; 4) It takes more storage to store all duplicates

## 11. How many times will firebase-sdk fire on onAuthStateChanged subscription callback?

**Ans:** *At least once (when app loads). Any changes to authentication state will fire the callback (e.g., sign out)*

onAuthStateChanged is a real-time listener and it will run at least once when the app loads. Any changes to user authentication will trigger the callback (e.g., sign out)

## 12. Why use transactions when updating database?

**Ans:** *Transctions allow to commit multiple operations as one atomic action. If one operation fails then the whole action fails*

Transcation means an atomic read/write action. Imagine you must update data in 3 different database locations. For that you need to perform 3 write operations. To ensure that data will be updated in all places, you would use a transcation. It is either all or nothing. If data was successfully updated in one location, but failed in other, the transcation will fail and eventually nothing will be updated. The update will only take place if all 3 operations succeed.

## 13. How can you specify what place to update in firebase real-time database?

**Ans:** *I must specify database place as a path as a path-string: /path/to/some/place/*

To update firebase realtime database you must specify database path in form of /path/to/some/place. Because database is JSON-based it's roughly equivalent how you access javascript object keys.

## 14. When does clean-up function of useEffect run?

**Ans:** *When one of the dependencies inside the dependency array changes*

useEffect's cleanup function runs when of the dependencies inside the dependency array changes. It cleans up the previous state of the effect.

## 15. How you cna partially select from the context object (value) when using Context API?

**Ans:** *No way to do that with raw Context API. Must use third-party packages (e.g., context selector) or somehow implement it manually*

Context API does not allow to select partial context value selection. Must use a library or implement the selecton logic manually.

## 16. You created a single context and you use it multiple times on different pages. If value in of the context instances changes, how other context values are affected?

**Ans:** *Other values will not be affected*

They are not affected. Every context instance is not aware of the other one. Changing value inside one context instance does NOT affect values inside other context isntances.

## 17. Why it is important to write security rules in firebase?

**Ans:** *To prevent unwanted access to the database*

If security rules were not properly written, any unwanted read/write access to a database location can take place. For instance: 1) user A can update profile of user B; 2) private user data can be leaked to the public (e.g., date of birth, personal address, phone number). Very important to remember that the app or website you develop is not the only way to access the database. Ther are public database URL and manual http requests.

## 18. What is auth object credential in firebase-sdk (the one you get from onAuthStateChanged)?

**Ans:** *Auth object represents currently authenticated use (user session)*

Auth object represents currently authenticated user. You can access auth user data using this object (e.g., email or social media providers)

## 19. When we bind a new event handler to an element (e.g., onChange), we receive an event object. What is this event object?

**Ans:** *Event object descibes an event. It has all event-related info such as event target, value and many others.*

Event object represents an event that occurs. For every event, this object is unique (e.g., when onChange event fires two times, it will produce two different event objects). The event object has all info about the event: target element, event value, event state, etc.

## 20. What is the benefit of using programmatical media query (useMediaQuery) instead of CSS?

**Ans:** *Allows to conditionally render elements because the result is a just a boolean (e.g., can conditionally pass dynamic classes to className)*

With an advantage of programmatical access to media queries, we are able to conditionally render elements inside components. We receive a boolean value that indicates whether the media query satisfies the condition.