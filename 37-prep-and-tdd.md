# Read37:   Redux - Combined Reducers
* Multiple Reducers Example .
* Redux Docs: Using Combined Reducers .
* Redux Docs: Combined Reducer Syntax.

### *Multiple Reducers Example*

- a basic redux application, for example, watch this video [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE).

### *Redux Docs: Using Combined Reducers*

- Core Concepts:

the most common state shape for a Redux app is a plain Javascript object containing "slices" of domain-specific data at each top-level key. Similarly, the most common approach to writing reducer logic for that state shape is to have "slice reducer" functions, each with the same (state, action) signature, and each responsible for managing all updates to that specific slice of state. Multiple slice reducers can respond to the same action, independently update their own slice as needed, and the updated slices are combined into the new state object.

Because this pattern is so common, Redux provides the combineReducers utility to implement that behavior. It is an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function.

- Defining State Shape

There are two ways to define the initial shape and contents of your store's state. First, the createStore function can take preloadedState as its second argument. This is primarily intended for initializing the store with state that was previously persisted elsewhere, such as the browser's localStorage. The other way is for the root reducer to return the initial state value when the state argument is undefined. 


For more details see  [Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/).

### *Redux Docs: Combined Reducer Syntax*

- The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

Example: 

         rootReducer = combineReducers({potato: potatoReducer, tomato: tomatoReducer})
         // This would produce the following state object
         {
           potato: {
             // ... potatoes, and other state managed by the potatoReducer ...
              },
           tomato: {
            // ... tomatoes, and other state managed by the tomatoReducer, maybe some nice sauce? ...
            }
           }

For more details see [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/).
