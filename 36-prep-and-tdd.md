# Read36: Application State with Redux
* Application State with Redux .

### *Application State with Redux*
 
- Redux provides a solid, stable, and mature solution to managing state in your React application. Through a handful of 
small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a 
delightfully organized, easy to understand modern JavaScript powerhouse.

- Redux is a predictable state container for JavaScript apps. As the application grows, it becomes difficult to keep it 
organized and maintain data flow. Redux solves this problem by managing application’s state with a single global object 
called Store. Redux fundamental principles help in maintaining consistency throughout your application, which makes debugging 
and testing easier.

- Principles of Redux:

1. Single Source of Truth

The state of your whole application is stored in an object tree within a single store. As whole application state is stored 
in a single tree, it makes debugging easy, and development faster.

2. State is Read-only

The only way to change the state is to emit an action, an object describing what happened. This means nobody can directly 
change the state of your application.

3. Changes are made with pure functions

To specify how the state tree is transformed by actions, you write pure reducers. A reducer is a central place where state 
modification takes place. Reducer is a function which takes state and action as arguments, and returns a newly updated state.

- Redux - Installation :

To install redux

Run the following command in your command prompt to install Redux.

          npm install --save redux

To use Redux with react application, you need to install an additional dependency as follows −

          npm install --save react-redux          

- Redux components are as follows −

![redux](https://www.tutorialspoint.com/redux/images/data_handling_logic.jpg)

- Redux - Data Flow

Redux follows the unidirectional data flow. It means that your application data will follow in one-way binding data flow. As 
the application grows & becomes complex, it is hard to reproduce issues and add new features if you have no control over the 
state of your application.

Redux reduces the complexity of the code, by enforcing the restriction on how and when state update can happen. This way, 
managing updated states is easy. We already know about the restrictions as the three principles of Redux.

![redux](https://www.tutorialspoint.com/redux/images/data_flow.jpg)


For more details see [Application State with Redux](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867).
