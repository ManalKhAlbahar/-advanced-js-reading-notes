# Read28 : Component Lifecycle / useEffect() Hook
* effects hook .

### *effects hook*

- Using the Effect Hook:

There are two common kinds of side effects in React components: those that don’t require cleanup, and those that do.

- Effects Without Cleanup

  Sometimes, we want to run some additional code after React has updated the DOM. Network requests, manual DOM mutations, and 
  logging are common examples of effects that don’t require a cleanup. We say that because we can run them and immediately forget 
  about them. Let’s compare how classes and Hooks let us express such side effects.

-  Example Using Classes :

In React class components, the render method itself shouldn’t cause side effects

       class Example extends React.Component {
       constructor(props) {
        super(props);
        this.state = {
          count: 0
         };
            }

           componentDidMount() {
          document.title = `You clicked ${this.state.count} times`;
            }
            componentDidUpdate() {
           document.title = `You clicked ${this.state.count} times`;
            }

            render() {
           return (
             <div>
               <p>You clicked {this.state.count} times</p>
              <button onClick={() => this.setState({ count: this.state.count + 1 })}>
                Click me
                </button>
                 </div>
                    );
                         }
                    } 

 - Example Using Hooks              

         import React, { useState, useEffect } from 'react';

         function Example() {
          const [count, setCount] = useState(0);

          useEffect(() => {
         document.title = `You clicked ${count} times`;
              });

         return (
             <div>
               <p>You clicked {count} times</p>
              <button onClick={() => setCount(count + 1)}>
               Click me
               </button>
               </div>
                );
                 }

- What does useEffect do? By using this Hook, you tell React that your component needs to do something after render. React will 
remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this 
effect, we set the document title, but we could also perform data fetching or call some other imperative API.

- Tips for Using Effects

useEffect that experienced React users will likely be curious about. Don’t feel obligated to dig into them now. You can always come 
back to this page to learn more details about the Effect Hook.

- Effects with Cleanup

       Example Using Classes:

              class FriendStatus extends React.Component {
          constructor(props) {
         super(props);
         this.state = { isOnline: null };
        this.handleStatusChange = this.handleStatusChange.bind(this);
       }

           componentDidMount() {
           ChatAPI.subscribeToFriendStatus(
            this.props.friend.id,
             this.handleStatusChange
            );
          }
          componentWillUnmount() {
           ChatAPI.unsubscribeFromFriendStatus(
            this.props.friend.id,
            this.handleStatusChange
             );
           }
             handleStatusChange(status) {
              this.setState({
              isOnline: status.isOnline
               });
               }

          render() {
           if (this.state.isOnline === null) {
               return 'Loading...';
             }
               return this.state.isOnline ? 'Online' : 'Offline';
             }
              }

Notice how componentDidMount and componentWillUnmount need to mirror each other. Lifecycle methods force us to split this logic even 
though conceptually code in both of them is related to the same effect.

- Why did we return a function from our effect? This is the optional cleanup mechanism for effects. Every effect may return a 
function that cleans up after it. This lets us keep the logic for adding and removing subscriptions close to each other. They’re 
part of the same effect!

For more details see [effects hook](https://reactjs.org/docs/hooks-effect.html).

