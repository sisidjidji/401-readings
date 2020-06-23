## Custom Hooks

### 1. What are custom hooks?

* Extract duplicated logic from components
* Share common functionality
* But not state…
* Take advantage of useEffect lifecycle

### 2. Common use cases – make things DRY!

* Handle forms easily
* Pre-fetch API data
* Connect to services (like socket.io, Q, etc)


* Hooks are an additive change to the core library. Meaning they are opt-in and backward compatible. They have gone through a Request For Comments process on GitHub before being released. If you want to use them, simply install the latest version of React.

* The Hook pattern provides an alternative to writing class-based components and a simple to use state and has an alternative for lifecycle methods. Hooks bring to functional components the things we once were only able to do with classes, like being able to work with React local state, effects and context through useState, useEffect and useContext.


### 3. Five Important Rules for Hooks

Before we create our own Hook, let's review a few of the major rules we must always follow.

1. Never call Hooks from inside a loop, condition or nested function
2. Hooks should sit at the top-level of your component
3. Only call Hooks from React functional components
4. Never call a Hook from a regular function
5. Hooks can call other Hooks