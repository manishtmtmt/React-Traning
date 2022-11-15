## 1. What is a denormalized data?

**Ans:** *Denormalized data is duplicated data in multiple database locations*

Denormalized data is a concept of NoSQL database that implies data duplication in multiple places in order to avoid multiple queries when data is requested. This concept is a normal NoSQL practice and is encouraged. Denormalization adds another layer of complexity and is one of the main trade-offs of NoSQL databases.

## 2. Why do we need denormalized data?

**Ans:** *To prevent multiple database queries and optimize read performance*

Since there is no SQL-like joins available in NoSQL databases, data denormalization is the most efficient approach to prevent sending multiple queries to the database. Related data is grouped and stored together. It's like storing SQL-join results upfront. Imagine a book record. Every book is associated with an author. Normally, you want to store author id next to book data, however, if you want to display author data next to the book, knowing only author ID you can't do that because there is no SQL-like joins in NoSQL world. You need to send another request to get author profile data. To avoid this kind of situations, instead of author ID, you would store author data that you want to display.

## 3. If there is a real-time listener in React (subscription), how to properly handle it?

**Ans:** *Subscribe and unsubscribe to the listener inside useEffect*

The best and correct way to handle subscriptions in React is useEffect and only useEffect. For every real-time listener, there must be a function that lets you to unsubscribe from the listener. If not handled properly, you will end up with memory leaks.

## 4. How to directly manipulate an HTML element in React?

**Ans:** *Using the useRef hook*

useRef is the best way to keep reference of DOM node (html element) in React. The result is the same as if it was document.getElementById, but unlike latter, if something happens to the element, reference to the element will reflect those changes. document.getElementById can be certainly used, but in 98% cases it's a bad smell.

## 5. Write negative consequences of bad security rules for firebase database?

**Ans:** *Database will suffer from unwanted read/write access and can leak private data*

If security rules were not properly written, any unwanted read/write access to a database location can take place. For instance: 1) user A can update profile of user B; 2) private user data can be leaked to the public (e.g. date of birth, personal address, phone number). Very important to remember that the app or website you develop is not the only way to access the database. There are public database URL and manual http requests.

## 6. Why use transactions when working with database?

**Ans:** *Transactions allow to commit multiple operations as one atomic action. If one operation fails then the whole action fails*

Transaction means an atomic read/write action. Imagine you must update data in 3 different database locations. For that, you need to perform 3 write operations. To ensure that data will be updated in all places, you would use a transaction. It is either all or nothing. If data was successfully updated in one location but failed in other, the transaction will fail and eventually, nothing will be updated. The update will only take place if all 3 operations succeed.