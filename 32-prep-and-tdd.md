# Read31:  Context API - Behaviors
* context api .

### *context api*

- Context API is a state management tool bundled with the React.js library itself.
- In React, a website is build using components. A component may consist of states, and functions.
- When to Use Context

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated 
user, theme, or preferred language. 

- Before You Use Context

context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly 
because it makes component reuse more difficult.

If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

For example, consider a Page component that passes a user and avatarSize prop several levels down so that deeply nested Link and 
Avatar components can read it:

            <Page user={user} avatarSize={avatarSize} />
         // ... which renders ...
          <PageLayout user={user} avatarSize={avatarSize} />
         // ... which renders ...
            <NavigationBar user={user} avatarSize={avatarSize} />
         // ... which renders ...
          <Link href={user.permalink}>
         <Avatar user={user} size={avatarSize} />
         </Link>

It might feel redundant to pass down the user and avatarSize props through many levels if in the end only the Avatar component 
really needs it. It’s also annoying that whenever the Avatar component needs more props from the top, you have to add them at all 
the intermediate levels too.         

One way to solve this issue without context is to pass down the Avatar component itself so that the intermediate components don’t 
need to know about the user or avatarSize props:
 
      function Page(props) {
     const user = props.user;
      const userLink = (
      <Link href={user.permalink}>
      <Avatar user={user} size={props.avatarSize} />
      </Link>
      );
     return <PageLayout userLink={userLink} />;
      }

      // Now, we have:
      <Page user={user} avatarSize={avatarSize} />
      // ... which renders ...
       <PageLayout userLink={...} />
       // ... which renders ...
       <NavigationBar userLink={...} />
       // ... which renders ...
      {props.userLink}

With this change, only the top-most Page component needs to know about the Link and Avatar components’ use of user and 
avatarSize.   

* API

1. React.createContext

         const MyContext = React.createContext(defaultValue);

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This default value 
can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause 
consuming components to use defaultValue.

2. Context.Provider 

        <MyContext.Provider value={/* some value */}>

Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.

The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.

3. Class.contextType

          class MyClass extends React.Component {
          componentDidMount() {
          let value = this.context;
         /* perform a side-effect at mount using the value of MyContext */
         }
          componentDidUpdate() {
         let value = this.context;
          /* ... */
          }
         componentWillUnmount() {
         let value = this.context;
         /* ... */
          }
         render() {
          let value = this.context;
         /* render something based on the value of MyContext */
          }
          }
           MyClass.contextType = MyContext;

The contextType property on a class can be assigned a Context object created by React.createContext(). Using this property lets you 
consume the nearest current value of that Context type using this.context. You can reference this in any of the lifecycle methods 
including the render function. 

4. Context.Consumer

          <MyContext.Consumer>
          {value => /* render something based on the context value */}
          </MyContext.Consumer>

 A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.  

5. Context.displayName

Context object accepts a displayName string property. React DevTools uses this string to determine what to display for the 
context.    

           const MyContext = React.createContext(/* some value */);
          MyContext.displayName = 'MyDisplayName';
            
          <MyContext.Provider> // "MyDisplayName.Provider" in DevTools
         <MyContext.Consumer> // "MyDisplayName.Consumer" in DevTools


For more details see [context api](https://reactjs.org/docs/context.html).

For more examples see [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b).

