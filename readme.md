## 🌟 For Developers (rafce)
```html
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
```
# Parcer App SetUp
```bash
  mkdir my-react-parcel-app
  cd my-react-parcel-app
  npm init -y
  npm install --save-dev parcel
  npm install react react-dom
  mkdir src
  touch src/index.jsx index.html
  "scripts": 
  {
  "dev": "parcel index.html",
  "build": "parcel build index.html"
  }
  npm run dev
```

---
## here is all the Terms of Reacts
```bash
https://gist.github.com/navneetpathak1/993a92f04d925894e9833d906a977f2d
```

## 📦 Popular Bundlers for React

- **Webpack**  
  A highly configurable and powerful bundler.  
  🔹 Extensive plugin system  
  🔹 Steeper learning curve but extremely flexible.

- **Parcel**  
  Known for its *zero-config* setup and simplicity.  
  🔹 Great for small-to-medium projects  
  🔹 Quick to start without heavy setup.

- **Vite**  
  A blazing-fast modern bundler.  
  🔹 Uses native ES modules during development  
  🔹 Ultra-fast dev server and build times.

---

## 📥 Install Parcel (as a dev dependency)

```bash
npm init
npm install -D parcel
npm install react
npm install react-dom
```
## How to run
```bash
npx parcel index.html
```
---

## 🌟 Caret (`^`) vs Tilde (`~`) in `package.json`

| Symbol | Meaning |
|:------:|:--------|
| `^` | Allows updates that do not change the first non-zero version (e.g., `^1.2.3` → accepts `1.x.x` but not `2.x.x`) |
| `~` | Allows patch-level updates only (e.g., `~1.2.3` → accepts `1.2.x`, but not `1.3.x`) |

> **Tip:**  
> Use `^` for most dependencies to stay updated with minor releases.  
> Use `~` when you need tighter control over updates.

---


### HMR

```bash
Hot Module Reloading
```


### File Watcher Algorithm 
```bash
written in c++
```
It’s an algorithm that monitors files or folders for any changes like:

    - Created

    - Modified

    - Deleted

When a change happens → it triggers an action (like rebuild, reload, etc.).
(That's how Parcel, Vite, etc. detect when you save a file.)


## if you want to remove your console log =>
babel-plugin-transform-remove-console
run

```bash
npm install babel-plugin-transform-remove-console --save-dev
```
---
make .babelrc file
```bash
{
  "plugins": [ ["transform-remove-console", { "exclude": [ "error", "warn"] }] ]
}
```
---
---

babel convert 
```bash 
https://babeljs.io/
```
```bash
const heading4 = (
  <h1 key="n"> Hello world : </h1>
)
```
==>
```bash
  const heading4 = React.createElement("h1", { key: "n" }, "Hello world");
```
---

React Component
- Class Based Component => Old way 
- Functional => new way

---

## Component Composition 
```bash
const App = () => {
    return (
        <div>
            <Header /> // => Component Composition
            <Content />
            <Footer />
        </div>
    );
}; 
```
---
### Read about **Cross Site Scripting (XSS)**
---
# Important
```<React.Fragment> <React.Fragment/>```
we can also write it as
```<></> ```
---
Know more about
- ***Config Driven UI***
- ***Virtual Dom***
- ***Reconciliation ***
- ***React Fiber Architecture*** 



## monolithic and microservices architecture

- Monolithic: Complete project in one place all APIs, UI, Auth, DB all things are in one project only, So if need to change color of a button then again deploy all project

- Microservices: ***single responsibility principle***, ***separation of concern***

---

***So how We communicate with these different different services:***
Different different services are operate on different different port, And we communicate using these port.

there are two main approach to do so:
- 1. Loads -> API call -> Render UI
- 2. Loads -> Render -> API call -> Render  (Better)  => useEffect


In **useEffect** - if no dependency array then useEffect is called every re-render
                 - if empty dependency array then only once
                 - if some value inside dependency array then only when the value changes
---

## Shimmer UI || Skeleton UI
---

## react-router-dom

- createBrowserRouter
- createBrowserRouter
- Outlet
- Link
- useRouteError
- useParams

- **Single page application**

# Two types of routing in web page
1. Sever side routing => for single page
2. Client side routing


---

# Optimizing our App

## custom hooks

---

## addEventListener version
```bash
window.addEventListener("offline", (event) => {
  console.log("The network connection has been lost.");
});
```
---
 
- Chunking
- Code Splitting
- Dynamic Bundling
- lazy loading
- on demand loading
- dynamic import
```
lazy
Suspense
```

---
## Styling React
- plain css
- Sass
- styled components
- material ui
- bootstrap 
- tailwind css 

---

## Higher-Order Components
- Controlled and uncontrolled components
---
### Accordion features
---

## Lifting State Up
---
## Prop drilling
## createContext
## useContext
## .Provider
## .consumer
---

# zustand
# Redux
# Redux Toolkit
---
## Redux ToolKit

```
When you click on the button, it dispatches the action, which calls the reducer function that updates the slice of Redux Toolkit state.
In order to access it subscribe to the store using a selector
```
```bash
npm i @reduxjs/toolkit
npm i react-redux
```

Some jargons
- ***configureStore***
- ***provider***
- ***createSlice***
- ***useSelector***
- ***useDispatch***
- ***Immer***
- ***Redux toolkit***
- ***RTK Query***


---

# Testing
## Types of Testing in Web Applications
1. Unit Testing
2. Integration Testing
3. End-to-End (E2E)

---
## React Testing Library
```bash
npm install --save-dev @testing-library/react @testing-library/dom
```

## jest
```bash
npm install --save-dev jest
npm install --save-dev babel-jest @babel/core @babel/preset-env
```
In root make babel.config.js and past it
```bash
module.exports = {
  presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
};
```

**remove conflict** [link](https://parceljs.org/languages/javascript/#babel) configure parcel to disable default babel transpilation
**jest configuration**
```
npx create-jest
```
**jsdom** -> yes for coverage report -> babel -> yes for clear...

## install jsdom using ***npm install --save-dev jest-environment-jsdom***
## install ***@babel/preset-react*** to make jsx work in test case
## install @testing-library/jest-dom
---


- make __tests__ folder
- file must be like
  - header.test.js
  - header.test.ts
  - header.spec.js
  - header.spec.ts

_ _  = Dunder


---

## Form validation in react use ***Formik***

---
***useRef***
***memoization***