<div align="center">
  <h1>50 ReactJS Concepts</h1>
  
  <p><b>ReactJs</b> is a free and open-source front-end JavaScript library for building user interfaces based on components.</p>
  
  <img src="https://miro.medium.com/max/1400/1*KN7zbaWkbm5E71zZWfTf7A.gif" alt="reactjs-banner">
</div>

<br>

# Let's go :)

1. [Why React](#1-why-react)
2. [Static vs Dynamic vs SPA](#2-Static-vs-Dynamic-vs-SPA) 
3. [Why React is a library](#3-Why-React-is-a-library)
4. [Virtual DOM](#4-Virtual-DOM)

## 1. Why React?
With React, first we can built the components, then we can connect them together.

**[⬆ Back to Top](#lets-go-)**

## 2. Static vs Dynamic vs SPA
#### Static: 
1. Static webpages are the `prebuilt/pre-uploaded` files that gets served when the user requested.
2. When we navigate to a specific route, page reloads & the new html file gets served.
3. Static sites are very fast but they only make sense when your content changes infrequently.

#### Dynamic:
1. These sites generate HTML on the server side through the use of `templating engines` or a language like PHP.
2. The content is generated per request and is served slower than its static site counterpart.
3. The main advantage of a dynamic website is that they do not need to be rebuilt. When your data changes, the content will be shown updated on the next refresh.

#### Single Page Applications:
1. SPAs are applications built in a manner that does not reload the entire page when navigating the site's routes.
2. It is a single file that served to the client. It doesn't reload the page rather re-renders the page contents.
3. Not good for SEO becoz a web crawler may not wait for the JavaScript to finish executing before it is finished crawling.

## 3. Why React is a library?
React deals with the `views` & let's us choose the reest of the front-end architecture.

But by adding few more libraries, we can build a complete app easily & also react has the best community around it.

## 4. Virtual DOM:
Let us first understand DOM, it is Document Object Model. It is a structural representation of the HTML elements. 
DOM represents the entire UI of the applicaton.

Without React we can directly manipulate the DOM elements which results in frequent DOM manipulation, and each time an update was made the browser had to re-calculate & repaint the whole view accr to the new content.So React brought us Virtual DOM, which can be refered as the copy of the actual DOM. 

The `virtual DOM` (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called `reconciliation`.

## 5. Shadow DOM:
The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components.

## 6. React DOM:
Its a package that provides DOM specific methods to manage the DOM elements. It provides some APIs or methods, such as render, find DOM node etc.
```javascript
ReactDOM.render(
  <React>
    <App/>
  </React>, document.getElementById('root')
);
```

## 7. JSX
1. Stands for JavaScript XML.
2. It just provides `syntactic sugar` for the React createElement function.
3. JSX made easy to write both HTML & JavaScript together.
4. But browsers cannot understand the JSX, so we have to use transpilers(Babel) to convert JSX to browser understandable code.
4. You are not required to use JSX, but JSX makes it easier to write React applications.

#### Without JSX:
```javascript
const myElement = React.createElement('h1', {}, 'I do not use JSX!');

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
#### With JSX:
```javascript
const myElement = <h1>I Love JSX!</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

## 8. XML
Stands for Xtensible markup language.

HTML is a Markup language but XML provides framework to define markup languages.

## 9. Class Life Cycle Methods
1. **Mounting** : constructor, static getDerivedStateFromProps, render & componentDidMount.
2. **Updating**: static getDerivedStateFromProps, render, shouldComponentUpdate, getSnapshotBeforeUpdate, componentDidUpdate.
3. **Unmounting**: componentWillUnmount.
4. **Error handling**: static getDerivedStateFromError & componentDidCatch.

## 10. React Hooks
Introduced in React 16.8.

Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed.

#### Basic Hooks
1. useState - useState lets you manage local state within a function component.
2. useEffect - With useEffect, you invoke side effects from within functional components.
3. useContext - Context is React’s way of handling shared data between multiple components.

#### Additional Hooks
4. useReducer - useReducer may be used as an alternative to useState. It’s ideal for complex state logic.
5. useCallback - useCallback returns a memoized callback function.
6. useMemo - useMemo Hook returns a memoized value.
7. useRef - The useRef Hook allows you to persist values between renders.
8. useImperativeHandle - useImperativeHandle is a React Hook that lets you customize the handle exposed as a ref.
9. useLayoutEffect - useLayoutEffect is a version of useEffect that fires before the browser repaints the screen.
10. useDebugValue - useDebugValue Hook helps developers to debug custom hooks in Devtools.
11. useDeferredValue - useDeferredValue is a React Hook that lets you defer updating a part of the UI.
12. useTransition - useTransition is a React Hook that lets you update the state without blocking the UI.
13. useId - useId is a React Hook for generating unique IDs that can be passed to accessibility attributes.

#### Library Hooks
14. useSyncExternalStore - useSyncExternalStore is a React Hook that lets you subscribe to an external store.
15. useInsertionEffect - useInsertionEffect is a version of useEffect that fires before any DOM mutations.
