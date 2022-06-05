# Read39:   Redux - Additional Topics
* Redux Toolkit (RTK) .
* MobX .
* HookState.

### *Redux Toolkit (RTK)*

- Getting Started with Redux Toolkit:

- The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

     - "Configuring a Redux store is too complicated"
     - "I have to add a lot of packages to get Redux to do anything useful"
     - "Redux requires too much boilerplate code"

- Redux Toolkit also includes a powerful data fetching and caching capability that we've dubbed "RTK Query". It's included in the package as a separate set of entry points. It's optional, but can eliminate the need to hand-write data fetching logic yourself.

- Installation​

The recommended way to start new apps with React and Redux is by using the official Redux+JS template or Redux+TS template for Create React App, which takes advantage of Redux Toolkit and React Redux's integration with React components.

          # Redux + Plain JS template
         npx create-react-app my-app --template redux

          # Redux + TypeScript template
         npx create-react-app my-app --template redux-typescript

- An Existing App​
Redux Toolkit is available as a package on NPM for use with a module bundler or in a Node application:

        # NPM
         npm install @reduxjs/toolkit         

- Redux Toolkit includes these APIs:

1. configureStore(): wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
2. createReducer(): that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code, like state.todos[3].completed = true.
3. createAction(): generates an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.
4. createSlice(): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
5. createAsyncThunk: accepts an action type string and a function that returns a promise, and generates a thunk that dispatches pending/fulfilled/rejected action types based on that promise
6. createEntityAdapter: generates a set of reusable reducers and selectors to manage normalized data in the store
7. The createSelector utility from the Reselect library, re-exported for ease of use.

- RTK Query is provided as an optional addon within the @reduxjs/toolkit package. It is purpose-built to solve the use case of data fetching and caching, supplying a compact, but powerful toolset to define an API interface layer for your app. It is intended to simplify common cases for loading data in a web application, eliminating the need to hand-write data fetching & caching logic yourself.

- RTK Query is built on top of the Redux Toolkit core for its implementation, using Redux internally for its architecture. Although knowledge of Redux and RTK are not required to use RTK Query, you should explore all of the additional global store management capabilities they provide, as well as installing the Redux DevTools browser extension, which works flawlessly with RTK Query to traverse and replay a timeline of your request & cache behavior.

- RTK Query is included within the installation of the core Redux Toolkit package. It is available via either of the two entry points below:

            import { createApi } from '@reduxjs/toolkit/query'

         /* React-specific entry point that automatically generates
            hooks corresponding to the defined endpoints */
           import { createApi } from '@reduxjs/toolkit/query/react'

- RTK Query includes these APIs:

1. createApi(): The core of RTK Query's functionality. It allows you to define a set of endpoints describe how to retrieve data from a series of endpoints, including configuration of how to fetch and transform that data. In most cases, you should use this once per app, with "one API slice per base URL" as a rule of thumb.
2. fetchBaseQuery(): A small wrapper around fetch that aims to simplify requests. Intended as the recommended baseQuery to be used in createApi for the majority of users.
< ApiProvider />: Can be used as a Provider if you do not already have a Redux store.
3. setupListeners(): A utility used to enable refetchOnMount and refetchOnReconnect behaviors.           

For more details see [Redux Toolkit (RTK)](https://redux-toolkit.js.org/introduction/getting-started).

### *MobX*

- MobX is a simple, scalable and battle tested state management solution. This tutorial will teach you all the important concepts of MobX in ten minutes. MobX is a standalone library, but most people are using it with React and this tutorial focuses on that combination.

For more details see  [MobX](https://mobx.js.org/getting-started.html).

### *HookState*

- Getting started
     - Intuitive API. Most things will be self-explanatory. More in depth description will always be there.
     - Code samples in each section are self-contained, complete and interactive. So, jump to the relevant section, copy-paste a sample to your app and extend it as needed.
     - Intellisense by IDE. If your project is in Typescript, you will benefit a lot as type inference of the API functions supports any complexity of data structures of your states. Of course, you can also use it from plain javascript.
      - Complete demo application. There is a Todo-list-like complete demo application built with Hookstate. It uses and d emonstrates most of the core features of Hookstate.

- Installation and dependencies

      npm install --save @hookstate/core

- Browser support#

Hookstate supports all recent browsers and works where React works, including mobile applications and server side rendering.

For more details see  [HookState](https://hookstate.js.org/docs/getting-started).