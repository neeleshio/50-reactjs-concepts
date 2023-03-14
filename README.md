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

**[⬆ Back to Top](#lets-go-)**

## 3. Why React is a library?
React deals with the `views` & let's us choose the reest of the front-end architecture.

But by adding few more libraries, we can build a complete app easily & also react has the best community around it.

**[⬆ Back to Top](#lets-go-)**

## 4. Virtual DOM:
Let us first understand DOM, it is Document Object Model. It is a structural representation of the HTML elements. 
DOM represents the entire UI of the applicaton.

Without React we can directly manipulate the DOM elements which results in frequent DOM manipulation, and each time an update was made the browser had to re-calculate & repaint the whole view accr to the new content.So React brought us Virtual DOM, which can be refered as the copy of the actual DOM. 

The `virtual DOM` (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called `reconciliation`.

**[⬆ Back to Top](#lets-go-)**

## 5. Shadow DOM:
The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components.

**[⬆ Back to Top](#lets-go-)**

## 6. React DOM:
Its a package that provides DOM specific methods to manage the DOM elements. It provides some APIs or methods, such as render, find DOM node etc.
```javascript
ReactDOM.render(
  <React>
    <App/>
  </React>, document.getElementById('root')
);
```

**[⬆ Back to Top](#lets-go-)**

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

**[⬆ Back to Top](#lets-go-)**

## 8. XML
Stands for `Xtensible markup language`.

HTML is a Markup language but XML provides framework to define markup languages.

**[⬆ Back to Top](#lets-go-)**

## 9. Class Life Cycle Methods
1. **Mounting** : constructor, static getDerivedStateFromProps, render & componentDidMount.
2. **Updating**: static getDerivedStateFromProps, render, shouldComponentUpdate, getSnapshotBeforeUpdate, componentDidUpdate.
3. **Unmounting**: componentWillUnmount.
4. **Error handling**: static getDerivedStateFromError & componentDidCatch.

**[⬆ Back to Top](#lets-go-)**

## 10. React Hooks
Introduced in React 16.8.

Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed.

#### Basic Hooks
1. **useState** - useState lets you manage local state within a function component.
2. **useEffect** - With useEffect, you invoke side effects from within functional components.
3. **useContext** - Context is React’s way of handling shared data between multiple components.

#### Additional Hooks
4. **useReducer** - useReducer may be used as an alternative to useState. It’s ideal for complex state logic.
5. **useCallback** - useCallback returns a memoized callback function.
6. **useMemo** - useMemo Hook returns a memoized value.
7. **useRef** - The useRef Hook allows you to persist values between renders.
8. **useImperativeHandle** - useImperativeHandle is a React Hook that lets you customize the handle exposed as a ref.
9. **useLayoutEffect** - useLayoutEffect is a version of useEffect that fires before the browser repaints the screen.
10. **useDebugValue** - useDebugValue Hook helps developers to debug custom hooks in Devtools.
11. **useDeferredValue** - useDeferredValue is a React Hook that lets you defer updating a part of the UI.
12. **useTransition** - useTransition is a React Hook that lets you update the state without blocking the UI.
13. **useId** - useId is a React Hook for generating unique IDs that can be passed to accessibility attributes.

#### Library Hooks
14. **useSyncExternalStore** - useSyncExternalStore is a React Hook that lets you subscribe to an external store.
15. **useInsertionEffect** - useInsertionEffect is a version of useEffect that fires before any DOM mutations.

**[⬆ Back to Top](#lets-go-)**

## 11. Functional components
Functional components are stateless(No state & no side effects) components before hooks introduction.

**[⬆ Back to Top](#lets-go-)**

## 12. Why use functional components over class components?
In javascript, classes are not real classes, they are just syntactic sugar, behind they are actually functions itself.

Functions are straight forward, so 3 things actually motivated react team to introduce hooks to provide lifecycle features to functional components.
1. Complex components become hard to understand.
2. Classes confuse both humans and machines.
3. It's hard to resuse stateful logic b/w components.

In Javascript, the 'this' keyword acts differently than other language, so there will be some learning curve for someone who is coming from other languages.

**[⬆ Back to Top](#lets-go-)**

## 13. Prop drilling
Prop drilling refers to where we have to pass data/state from a top-level component to a deeply nested component.

**[⬆ Back to Top](#lets-go-)**

## 14. State vs Props
#### State:
1. States are plain Javascript objects. It allows components to create & manage their own data.
2. States are mutable.
3. State holds the information about the component.
4. State cannot be accessed by the child component.

#### Props:
1. Props are also a Javascript object which contains all the properties passed to the child components.
2. Props are Immutable.
3. Props allow us to pass data from one component to another component.
4. Props can be accessed by the child components.

**[⬆ Back to Top](#lets-go-)**

## 15. Strict mode.
It activates additional checks & warning for its decendents.

It highlights the potential problems in the application.

#### React strict mode renders twice?
Yes, in order to detect any problems with the code & warn you about them only in development mode.

**[⬆ Back to Top](#lets-go-)**

## 16. React optimisation techniques
1. **React.Fragments**:\
It avoids adding extra nodes to the DOM.

2. **React.Lazy & React.Suspense**:\
Lazy loading is a great technique for optimising & speeding up the render time of our app.\
The idea of lazy loading is to load components only when it is needed. `React.Suspense` allows us to add a fallback content as a loading state.

3. **React.Memo**:\
To memorize a component or to cache the component.

4. **Pagination**:
When we are rendering large amount of data, implementing pagination decreases the load on the DOM tree.

5. **React-window**(Virtualize long lists):
If we are rendering a very large list, implementing infinte scroll technique using `react-window` helps in rendering only visible lists.

6. **Using Throttling & debouncing techniques:

7. **Using a CDN**
This will be useful in delivering the static content more quickly & efficiently.
Cloudflare is an example.

8. **Web workers**:
Web workers makes it possible to run a script operation in a web browser's background thread, so that the main thread won't get blocked.

9. **Server-side rendering**:

10. **Lazy-loading images**:

11. **Code splitting**:

**[⬆ Back to Top](#lets-go-)**

## 17. Error boundries
Is the way to handle errors in react.

We can wrap any part of our application in a special component & if that part of our apllication experiences an uncaught error, it will be shown as error.
So we can log these errors & display a fallback UI. & it doesn't break our app.

To use error boundary, we have to write some boilerplate code with class component.

```javascript
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError(error) {
    // Update state so the next render will show the fallback UI.
    return { hasError: true };
  }

  componentDidCatch(error, errorInfo) {
    // You can also log the error to an error reporting service
    logErrorToMyService(error, errorInfo);
  }

  render() {
    if (this.state.hasError) {
      // You can render any custom fallback UI
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children; 
  }
}
```

If we don't want to write all these code, we can just use `react-error-boundary` npm package.

```javascript
npm i react-error-boundary
```

**[⬆ Back to Top](#lets-go-)**

## 18. One way vs Two way Binding.
Data Binding is the process of connecting the view element or user interface, with the data which populates it. ReactJS uses one-way data binding.

Data binding in React can be achieved by using a `controlled input`. A controlled input is achieved by binding the value to a state variable and a `onChange event` to change the state as the input value changes.

We can see two-way binding in `AngularJS`. Two-way binding gives components in your application a way to share data. Use two-way binding to listen for events and update values simultaneously between parent and child components.

**[⬆ Back to Top](#lets-go-)**

## 19. Controlled vs Uncontrolled components
In a `controlled component`, form data is handled by a React component. The alternative is `uncontrolled components`, where form data is handled by the DOM itself.

To write an uncontrolled component, instead of writing an event handler for every state update, you can use a ref to get form values from the DOM.

#### Controlled:
1. The component is under control of the component’s state.
2. These components are predictable as are controlled by the state of the component.
3. Controlled by the parent component.
4. Have better control on the form data and values

#### Uncontrolled:
1. Components are under the control of DOM.
2. Are unpredictable because during the life cycle methods the data may loss.
3. Controlled by the DOM itself.
4. Has very limited control over form values and data.

**[⬆ Back to Top](#lets-go-)**

## 20. 
