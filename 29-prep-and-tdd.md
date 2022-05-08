# Read29 : Advanced State with Reducers
* useReducer hook .
* Ultimate Guide to useReducer.


### *useReducer hook*

         const [state, dispatch] = useReducer(reducer, initialArg, init);

- An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a 
dispatch method.

- useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next 
state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because 
you can pass dispatch down instead of callbacks.

- Specifying the initial state :

There are two different ways to initialize useReducer state. You may choose either one depending on the use case. The simplest way 
is to pass the initial state as a second argument:

               const [state, dispatch] = useReducer(
           reducer,
          {count: initialCount}
           );        

  **Note**

React doesn’t use the state = initialState argument convention popularized by Redux. The initial value sometimes needs to depend on 
props and so is specified from the Hook call instead. If you feel strongly about this, you can call useReducer(reducer, undefined, 
reducer) to emulate the Redux behavior, but it’s not encouraged.

- Lazy initialization

You can also create the initial state lazily. To do this, you can pass an init function as the third argument. The initial state 
will be set to init(initialArg).

- useCallback 

Pass an inline callback and an array of dependencies. useCallback will return a memoized version of the callback that only changes 
if one of the dependencies has changed. This is useful when passing callbacks to optimized child components that rely on reference 
equality to prevent unnecessary renders (e.g. shouldComponentUpdate).

useCallback(fn, deps) is equivalent to useMemo(() => fn, deps).

- useMemo

        const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);

Returns a memoized value.

Pass a “create” function and an array of dependencies. useMemo will only recompute the memoized value when one of the dependencies 
has changed. This optimization helps to avoid expensive calculations on every render.

Remember that the function passed to useMemo runs during rendering. Don’t do anything there that you wouldn’t normally do while 
rendering. For example, side effects belong in useEffect, not useMemo.

If no array is provided, a new value will be computed on every render.

- useRef

       const refContainer = useRef(initialValue);

useRef returns a mutable ref object whose .current property is initialized to the passed argument (initialValue). The returned 
object will persist for the full lifetime of the component.       

- useImperativeHandle

           useImperativeHandle(ref, createHandle, [deps])

useImperativeHandle customizes the instance value that is exposed to parent components when using ref. As always, imperative code 
using refs should be avoided in most cases.          

- useLayoutEffect

The signature is identical to useEffect, but it fires synchronously after all DOM mutations. Use this to read layout from the DOM 
and synchronously re-render. Updates scheduled inside useLayoutEffect will be flushed synchronously, before the browser has a chance 
to paint.

- useDebugValue

            useDebugValue(value)


useDebugValue can be used to display a label for custom hooks in React DevTools.

- useDeferredValue

            const deferredValue = useDeferredValue(value);

useDeferredValue accepts a value and returns a new copy of the value that will defer to more urgent updates. If the current render 
is the result of an urgent update, like user input, React will return the previous value and then render the new value after the 
urgent render has completed.

- useId

           const id = useId();

useId is a hook for generating unique IDs that are stable across the server and client, while avoiding hydration mismatches.

- Library Hooks

useSyncExternalStore

useSyncExternalStore is a hook recommended for reading and subscribing from external data sources in a way that’s compatible with 
concurrent rendering features like selective hydration and time slicing.

This method returns the value of the store and accepts three arguments:
1. subscribe: function to register a callback that is called whenever the store changes.
2. getSnapshot: function that returns the current value of the store.
3. getServerSnapshot: function that returns the snapshot used during server rendering.

useInsertionEffect

The signature is identical to useEffect, but it fires synchronously before all DOM mutations. Use this to inject styles into the DOM 
before reading layout in useLayoutEffect. Since this hook is limited in scope, this hook does not have access to refs and cannot 
schedule updates.

For more details see [useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer).

### *Ultimate Guide to useReducer*

- useReducer is one of the additional Hooks that shipped with React v16.8. An alternative to the useState Hook, useReducer helps you 
manage complex state logic in React applications. When combined with other Hooks like useContext, useReducer can be a good 
alternative to Redux, Recoil or MobX. In certain cases, it is an outright better option.

- How does the useReducer Hook work?

The useReducer Hook is used to store and update states, just like the useState Hook. It accepts a reducer function as its first 
parameter and the initial state as the second.

useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later 
invoke it. While this is similar to the pattern Redux uses, there are a few differences.

- There are three main building blocks in Redux:
1. A store: An immutable object that holds the application’s state data
2. A reducer: A function that returns some state data, triggered by an action type
3. An action: An object that tells the reducer how to change the state. It must contain a type property and can contain an optional 
payload property

- The reducer function

The JavaScript reduce() method executes a reducer function on each element of the array and returns a single value. The reduce() 
method accepts a reducer function, which 
itself can accept up to four arguments.

- The dispatch method

The dispatch function accepts an object that represents the type of action we want to execute when it is called. Basically, it sends 
the type of action to the reducer function to perform its job, which, of course, is updating the state.

The action to be executed is specified in our reducer function, which in turn, is passed to the useReducer. The reducer function 
will then return the updated state.  

- Bailing out of a dispatch

If the useReducer Hook returns the same value as the current state, React will bail out without rendering the children or firing 
effects because it uses the Object.is comparison algorithm.

- useState vs. useReducer

useState is a basic Hook for managing simple state transformation, and useReducer is an additional Hook for managing more complex 
state logic. However, it’s worth noting that useState uses useReducer internally, implying that you could use useReducer for 
everything you can do with useState.

 However, there are some major differences between these two Hooks. With useReducer, you can avoid passing down callbacks through different levels of your component. Instead, useReducer allows you to pass a provided dispatch function, which in turn will improve performance for components that trigger deep updates.

However, this does not imply that the useState updater function is newly called on each render. When you have a complex logic to update state, you simply won’t use the setter directly to update state. Instead, you’ll write a complex function, which in turn would call the setter with updated state.

Therefore, it’s recommended to use useReducer, which returns a dispatch method that doesn’t change between re-renders, and you can have the manipulation logic in the reducers.

It’s also worth noting that with useState, the state updater function is invoked to update state, but with useReducer, the dispatch function is invoked instead, and an action with at least a type is passed to it.

For more details see [Ultimate Guide to useReducer](https://blog.logrocket.com/react-usereducer-hook-ultimate-guide/).

