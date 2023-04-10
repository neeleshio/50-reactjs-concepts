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
5. [Shadow DOM](#5-Shadow-DOM)
6. [React DOM](#6-React-DOM)
7. [JSX](#7-JSX)
8. [XML](#8-XML)
9. [Class Life Cycle Methods](#9-Class-Life-Cycle-Methods)
10. [React Hooks](#10-React-Hooks)
11. [Functional components](#11-Functional-components)
12. [Why use functional components over class components](#12-Why-use-functional-components-over-class-components)
13. [Prop drilling](#13-Prop-drilling)
14. [State vs Props](#14-State-vs-Props)
15. [Strict mode](#15-Strict-mode)
16. [React optimisation techniques](#16-React-optimisation-techniques)
17. [Error boundries](#17-Error-boundries)
18. [One way vs Two way Binding](#18-One-way-vs-Two-way-Binding)
19. [Controlled vs Uncontrolled components](#19-Controlled-vs-Uncontrolled-components)
20. [React.memo](#20-React-memo)
21. [Forward ref](#21-Forward-ref)
22. [Context API vs Redux](#22-Context-API-vs-Redux)
23. [Redux]
24. [Redux side-effects]
25. [Middlewares]
26. [Redux toolkit]
27. [Redux persists]
28. [NextJS]
29. [React vs Nextjs]
30. [Nextjs rendering methods]
31. [Advantages of NextJs]
32. [Composition vs Inheritance]
33. [Keys]
34. [Thinking in React]
35. [Accessibility]
36. [Code Splitting]
37. [PropTypes]
38. [Reconciliation]
39. [Fragments]
40. [State mutation]
41. [Use of render()]
42. [useContext vs Redux]
43. [useState vs useReducer]
44. [useMemo vs useCallback]
45. [useEffect vs useLayoutEffect]
46. [useRef]
47. [useImperativeHandle]
48. [Styling in React]
49. [Custom Hook]
50. [React Router]

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

## 3. Why React is a library
React deals with the `views` & let's us choose the reest of the front-end architecture.

But by adding few more libraries, we can build a complete app easily & also react has the best community around it.

**[⬆ Back to Top](#lets-go-)**

## 4. Virtual DOM
Let us first understand DOM, it is Document Object Model. It is a structural representation of the HTML elements. 
DOM represents the entire UI of the applicaton.

Without React we can directly manipulate the DOM elements which results in frequent DOM manipulation, and each time an update was made the browser had to re-calculate & repaint the whole view accr to the new content. So React brought us Virtual DOM, which can be refered as the copy of the actual DOM. 

The `virtual DOM` (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called `reconciliation`.

**[⬆ Back to Top](#lets-go-)**

## 5. Shadow DOM
The Shadow DOM is a browser technology designed primarily for scoping variables and CSS in web components.

**[⬆ Back to Top](#lets-go-)**

## 6. React DOM
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

## 12. Why use functional components over class components
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

## 15. Strict mode
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
To memoize a component or to cache the component.

4. **Pagination**:
When we are rendering large amount of data, implementing pagination decreases the load on the DOM tree.

5. **React-window**(Virtualize long lists):
If we are rendering a very large list, implementing infinte scroll technique using `react-window` helps in rendering only visible lists.

6. **Using Throttling & debouncing techniques**:

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

## 18. One way vs Two way Binding
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

## 20. React memo
React Memo is a higher-order component that wraps around a component to memoize the rendered output and avoid unnecessary renderings. or,\
If our component renders the same result given the same props, we can wrap it in a React.memo HOC.

This improves performance because it memoizes the result and skips rendering to reuse the last rendered result.

There are two ways you can wrap your component with React.memo():

```javascript
const myComponent = React.memo((props) => {
    /* render using props */
});

export default myComponent;
```

```javascript
const myComponent = (props) => {
    /* render using props */
};

export const MemoizedComponent = React.memo(myComponent);
```

#### Characteristics:
1. Use this to wrap only the child components.
2. Memo only checks for prop changes.
3. It checks/compares both the type & value.

#### When not to use memo:
1. If the component is heavy & usually renders with different props.
2. The more often the component renders with the same props, the havier & more computationaly expensive the output is, we need memo.
3. Use profiling to measure the benefits of applying React.memo.
4. When we have a pure functional component, meaning it should output the same results with the same input.
5. Donot use when you have a component with often changing props becoz memo have to compares & that is an expensive operation.

**[⬆ Back to Top](#lets-go-)**

## 21. Forward ref
Used to pass the reference/ref from the parent component to the child component.

```javascript
const inputRef = useRef(null)

// inside parent component
<Child ref={inputRef} />

// inside child component
const Child = forwardRef((props, ref) => {
  <input ref={ref}/>
})
```

## 22. Redux
Redux is an open-source JavaScript library used to manage application state. A Predictable State Container for JS Apps.

The way Redux works is simple. There is a central store that holds the entire state of the application. Each component can access the stored state without having to send down props from one component to another.

#### How Redux works:
3 core components in Redux — actions, store, and reducers.

1. Actions: 
Actions are plain javascript objects. Actions are the only way you can send data from your application to your Redux store.

Actions are created via an action creator, which in simple terms is a function that returns an action. And actions are executed using the store.dispatch() method which sends the action to the store.

We dispatch an action & it includes a type property which indicates the type of action & the payload that contains the information.

```javascript
const setLoginStatus = () => {
  return {
    type: 'LOGIN',
    payload: {
      username: 'neelesh'
    }
  }
}

// setLoginStatus function is a `action creator` & its returned object is the `action`.
```

2. Reducer:
Reducer is a `pure function`. It is based on the reduce function in JavaScript, where a single value is calculated from multiple values. Reducers contains the business logic.

Once the action is dispatched, it reaches the reducer function. It takes the current state of the application, performs the action & return a new state. Then the new state gets stored the Store.

They do not change the data in the object passed to them or perform any side effect in the application. 

3. Store:
The Store is a central state which is again a JavaScript object that holds the application state.

It is highly recommended to keep only one store in any Redux application.

Actions performed on the state always return a new state. Thus, the state is very easy and predictable.

With Redux, there’s one general state in the store, and every component has access to the store. This eliminates the need to continuously pass state from one component to another.


**[⬆ Back to Top](#lets-go-)**

## 23. Context API vs React-Redux
Context provides a way to pass data through the component tree without having to pass props down manually at every level.

Context API helps in eleminating prop drilling & it is ideal for small applications. 

## 24. Redux side-effects
Redux inspired by functional programming & out of the box has no place for side effects. They must be always pure functions.

This brings us some questions:
1. How can we enable the state transition of an application via asynchronous actions?
2. How do we enable state transitions involving a request to a web server, or the use of a timer?.
3. How do we integrate our application state with the data generated by an asynchronous action, while complying with Redux’s architectural pattern?

However, redux middlewares makes it possible to intercept dispatched actions & add additional complex behaviour around them, including side effects.

We can use redux-thunk middleware or Redux toolkit that lets us write action creators with more complex & asynchronous logic.

We can still write asynchronous logic without using any middlewares but thats little messy, it's managable if it's just a small application otherwise better to use middlewares. (https://www.velotio.com/engineering-blog/asynchronous-calls-in-redux-without-middlewares)

## 25. Middlewares
Redux middlewares allows developers to intercept all actions dispatched from components before they are passed to the reducer function.

For ex., we might want to sanitize the user’s input before it reaches our store for further processing. This can be achieved via Redux middleware.

Unlike the reducer, middleware is not required to be a pure function, so the Thunk middleware can perform functions that trigger side effects without any problems.

## 26. Redux toolkit
Redux Toolkit is a the official, opinionated, batteries-included toolset for efficient Redux development. 

Includes utilities to simplify common use cases like store setup, creating reducers, immutable update logic, and more.

#### Advantages:
1. DRYs up your code.
2. You avoid recreating logic, saving time and resources.
3. It can create cleaner and more efficient code.

## 27. Redux persists
This allows to save the redux store into localstorage.

## 28. NextJS
Next.js is an open-source web development framework created by the private company Vercel providing React-based web applications with server-side rendering and static website generation.

## 29. React vs NextJs
| React | NextJs |
| 1. React is a Javascript library to build UI. | 1. NextJs is a React framework for building fullstack applications |
| 2. React uses client-side JavaScript to render pages | 2. Next.js uses server-side to pre-render every page |
| 3. When client requests the URL, first a blank HTML file will reach the client along with JS & CSS files | 3. HTML gets generated on the server & served to the client |
| 4. React doesn't require live server | 4. NextJs needs a live Nodejs server |

## 30. Nextjs rendering methods
By default, Next.js pre-renders every page. This means that Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript.

Next.js has two forms of pre-rendering: Static Generation and Server-side Rendering. The difference is in **when** it generates the HTML for a page.

#### 1. Statis Site Generation (SSG):
The HTML page is generated at build time, i.e when we run `next build`. This HTML will then be reused on each request. It can be cached by a CDN.

```javascript
const About = () => {
  return <div> About </div>
}

export default About;
```

#### 2. Server-side Rendering (SSR):
The HTML is generated on each request.

SSR should be used when we need to fetch data from the API. NextJs provides a method for data fetching called `getServerSideProps`.

```javascript
export default function Page({ data }) {
  // Render data...
}

// This gets called on every request
export async function getServerSideProps() {
  const res = await fetch(`https://.../data`)
  const data = await res.json()

  // Pass data to the page via props
  return { props: { data } }
}
```

one drawback of SSR with data fecthing is, Everytime anyone requests this perticular page, the server has to go out & make a new request to the API to get the data.
This results in more work for the server & also more cost for if any 3rd party APIs.

If we don't want the page to get updated every single time, we can use ISR (Incremental Static Regeneration).

#### 3. Incremental Static Regeneration (ISR):
This is same as SSR except it `includes Caching`. So, instead of getServerSideProps here it uses `getStaticProps`.

```javascript
export const getStaticProps = () => {
  const res = await ........;
  
  return {
    props: {
      person: res.person
    },
    revalidate: 10
  }
}
```

When user A requests the webpage, he gets served the page with getStaticProps. So when another user requests the same page within the revalidate period (here it is 10sec), he gets served the same static page & not the newly generated page. Once 10sec elapsed, users will get served a new page once they request.

#### 4. Client Side Rendering (CSR):
Yes, CSR is also possible. Syntax will be just like React using useEffect.

```javascript
const CSR = () => {
  const [person, setPerson] = useState("")
  
  useEffect(() => {
    axios.get('https://some.com').then(res => {
      setPerson(res.data.person)
    })
  }, [])
  
  return (
    <div> Hey Iam {person} </div> 
  )
}

export default CSR;
```
So the server returns the HTML page with only `Hey Iam` content & the once the HTML rendered on the browser, the api gets called & renders the name.

Drawback is again the SEO issue.

## 31. Advantages of NextJs
1. Out of the box routing. File system routing. app.js is the root.
2. Out of the box code splitting. Only the requested page will get served to the client.
3. Nextjs is a fullstack framework, so we can write both FE & BE in a single project.
4. Pre-rendering can result in better performance and SEO.
5. Out of the box image optimisation using Image tag.

## 32. Composition vs Inheritance
In Object-Oriented Programming, `composition` is a well-known concept. It describes a class that can refer to one or more objects of another class as instances rather than inheriting properties from a base class like `inheritance`.

Inheritance is an Object-Oriented Programming concept in JavaScript that allows us to inherit the features of a parent from the child.

React recommends Composition.

## 33. Keys
Keys help React identify which items have changed, are added, or are removed. 

Keys should be given to the elements inside the array to give the elements a stable identity.

React don’t recommend using indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state.

Note: If you choose not to assign an explicit key to list items then React will default to using indexes as keys.

## 34. Thinking in React
1. Break The UI Into A Component Hierarchy
2. Build A Static Version in React
3. Identify The Minimal (but complete) Representation Of UI State
4. Identify Where Your State Should Live
5. Add Inverse Data Flow

## 35. Accessibility
