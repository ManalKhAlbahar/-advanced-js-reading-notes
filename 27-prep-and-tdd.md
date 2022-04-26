# Read27 : Hook
* making sense of hooks .
* the state hook.
* hooks api.
* hooks api reference.

### *making sense of hooks*

- React hooks are special functions to extend the capabilities of functional components and give them the possibility to have 
lifecycle events and manage state.
- Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components. 
- Hooks let us organize the logic inside a component into reusable isolated units.
- If the React community embraces the Hooks proposal, it will reduce the number of concepts you need to juggle when writing React 
applications.
- React hooks allows us to take a Reactjs functional component and add state and lifecycle methods to it.
- With React hooks you can now reuse stateful logic and have a better separation of concerns.

For more details see [making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889).

### *the state hook*

- What is a Hook? A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets 
you add React state to function components. We’ll learn other Hooks later.

- What does calling useState do? It declares a “state variable” ,This is a way to “preserve” some values between the function calls 
-useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when 
the function exits but state variables are preserved by React.

- What do we pass to useState as an argument? The only argument to the useState() Hook is the initial state. Unlike with classes, 
the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a 
number for how many times the user clicked, so pass 0 as initial state for our variable. 

- What does useState return? It returns a pair of values: the current state and a function that updates it. This is why we write 
const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a 
pair.

For more details see [the state hook](https://reactjs.org/docs/hooks-state.html).

### *hooks api*

- But what is a Hook?

   Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes. 

- But what is a Hook?

     Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes. 

- Rules of Hooks

   - Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
   -  Only call Hooks from React function components. 

For more details see [hooks api](https://reactjs.org/docs/hooks-overview.html).

### *hooks api reference*

- Hooks API Reference.
- Basic Hooks
  useState

          const [state, setState] = useState(initialState);

   During the initial render, the returned state (state) is the same as the value passed as the first argument (initialState).
      
  The setState function is used to update the state. It accepts a new state value and enqueues a re-render of the component.

         setState(newState);

    During subsequent re-renders, the first value returned by useState will always be the most recent state after applying 
    updates.      

- Functional updates

    If the new state is computed using the previous state, you can pass a function to setState. The function will receive the previous value, and return an updated value.

- Lazy initial state
   The initialState argument is the state used during the initial render. In subsequent renders, it is disregarded. If the initial state is the result of an expensive computation

- Rules of Hooks
    Hooks are JavaScript functions, but they impose two additional rules:

  - Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
  - Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions.
  
For more details see [hooks api reference](https://reactjs.org/docs/hooks-reference.html).