# Read38:   Redux - Asynchronous Actions
* async actions .
* thunk middleware .
* redux thunk.

### *async actions*

- use the React-Redux library to let our React components interact with a Redux store, including calling useSelector to read Redux state, calling useDispatch to give us access to the dispatch function, and wrapping our app in a Provider component to give those hooks access to the store.

- So far, all the data we've worked with has been directly inside of our React+Redux client application. However, most real applications need to work with data from a server, by making HTTP API calls to fetch and save items.

- Example REST API and Client :

To keep the example project isolated but realistic, the initial project setup already included a fake in-memory REST API for our data (configured using the Mirage.js mock API tool). The API uses /fakeApi as the base URL for the endpoints, and supports the typical GET/POST/PUT/DELETE HTTP methods for /fakeApi/todos. It's defined in src/api/server.js.

The project also includes a small HTTP API client object that exposes client.get() and client.post() methods, similar to popular HTTP libraries like axios. It's defined in src/api/client.js.

We'll use the client object to make HTTP calls to our in-memory fake REST API for this section.

- Redux Middleware and Side Effects

By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:
1. Logging a value to the console
2. Saving a file
3. Setting an async timer
4. Making an AJAX HTTP request
5. Modifying some state that exists outside of a function, or mutating arguments to a function
6. Generating random numbers or unique random IDs (such as Math.random() or Date.now())

- Redux middleware were designed to enable writing logic that has side effects.

a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.

- Redux Async Data Flow

handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.

Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.

Earlier, we saw a diagram that represents the normal synchronous Redux data flow. When we add async logic to a Redux app, we add an extra step where middleware can run logic like AJAX requests, then dispatch actions. That makes the async data flow look like this:
![data](https://d33wubrfki0l68.cloudfront.net/08d01ed85246d3ece01963408572f3f6dfb49d41/4bc12/assets/images/reduxasyncdataflowdiagram-d97ff38a0f4da0f327163170ccc13e80.gif)

- Using the Redux Thunk Middleware

Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.

For more details see [async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic#example-rest-api-and-client).

### *thunk middleware*

 - Thunk middleware for Redux. It allows writing functions with logic inside that can interact with a Redux store's dispatch and getState methods.

 - Installation and Setup

          npm install redux-thunk

- What’s a thunk?!

A thunk is a function that wraps an expression to delay its evaluation.
 
          // calculation of 1 + 2 is immediate
           // x === 3
          let x = 1 + 2
               
           // calculation of 1 + 2 is delayed
          // foo can be called later to perform the calculation
          // foo is a thunk!
          let foo = () => 1 + 2


For more details see  [thunk middleware](https://github.com/reduxjs/redux-thunk).

### *redux thunk*

- What is a "thunk"?

The word "thunk" is a programming term that means "a piece of code that does some delayed work". Rather than execute some logic now, we can write a function body or code that can be used to perform the work later.

For Redux specifically, "thunks" are a pattern of writing functions with logic inside that can interact with a Redux store's dispatch and getState methods.

Using thunks requires the redux-thunk middleware to be added to the Redux store as part of its configuration.

Thunks are the standard approach for writing async logic in Redux apps, and are commonly used for data fetching. However, they can be used for a variety of tasks, and can contain both synchronous and asynchronous logic.

- Writing Thunks

A thunk function is a function that accepts two arguments: the Redux store dispatch method, and the Redux store getState method. Thunk functions are not directly called by application code. Instead, they are passed to store.dispatch():

        const thunkFunction = (dispatch, getState) => {
        // logic here that can dispatch actions or read state
         }

           store.dispatch(thunkFunction)

A thunk function may contain any arbitrary logic, sync or async, and can call dispatch or getState at any time.

- Why Use Thunks?

Thunks allow us to write additional Redux-related logic separate from a UI layer. This logic can include side effects, such as async requests or generating random values, as well as logic that requires dispatching multiple actions or access to the Redux store state.

Redux reducers must not contain side effects, but real applications require logic that has side effects. Some of that may live inside components, but some may need to live outside the UI layer. Thunks (and other Redux middleware) give us a place to put those side effects.

It's common to have logic directly in components, such as making an async request in a click handler or a useEffect hook and then processing the results. However, it's often necessary to move as much of that logic as possible outside the UI layer. This may be done to improve testability of the logic, to keep the UI layer as thin and "presentational" as possible, or to improve code reuse and sharing.

In a sense, a thunk is a loophole where you can write any code that needs to interact with the Redux store, ahead of time, without needing to know which Redux store will be used. This keeps the logic from being bound to any specific Redux store instance and keeps it reusable.

For more details see  [redux thunk](https://redux.js.org/usage/writing-logic-thunks).