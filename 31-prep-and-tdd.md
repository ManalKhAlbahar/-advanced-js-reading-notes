# Read31:  Context API
* context api .

### *context api*

- Context provides a way to pass data through the component tree without having to pass props down manually at every level.
- In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain 
types of props that are required by many components within an application. Context provides a way 
to share values like these between components without having to explicitly pass a prop through every level of the tree.
- When to Use Context 

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated 
user, theme, or preferred language. 

- Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly 
because it makes component reuse more difficult.
- If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

#### API

* React.createContext

               const MyContext = React.createContext(defaultValue);

Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context 
value from the closest matching Provider above it in the tree.

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This default value 
can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause 
consuming components to use defaultValue.

* Context.Provider

        <MyContext.Provider value={/* some value */}>

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider 
can be connected to many consumers. Providers can be nested to override values deeper within the tree.

For more details see [context api](https://reactjs.org/docs/context.html).

For more details see [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b).

For more details see [react context links](https://github.com/diegohaz/awesome-react-context).
