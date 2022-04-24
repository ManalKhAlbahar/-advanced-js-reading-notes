# Read26 : Component Based UI
* React .
* react hello world.
* introducing JSX.
* rendering elements.

### *React*
- React :A JavaScript library for building user interface.

- React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will 
efficiently update and render just the right components when your data changes.

For more details see [React](https://reactjs.org).

### *react hello world*
- The smallest React example looks like this:

  ```json
     ReactDOM
     .createRoot(document.getElementById('root'))
      .render(<h1>Hello, world!</h1>);
  ```
It displays a heading saying “Hello, world!” on the page.

For more details see [react hello world](https://reactjs.org/docs/hello-world.html).

### *introducing JSX*
- JSX : it is a syntax extension to JavaScript.It used with React to describe what the UI should look like. JSX may remind you of a 
template language, but it comes with the full power of JavaScript.
- JSX produces React “elements”. 
- Why JSX?

React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

- JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.
- JSX converts HTML tags into react elements.
- Expressions in JSX : With JSX you can write expressions inside curly braces { }.
- The expression can be a React variable, or property, or any other valid JavaScript expression. JSX will execute the expression and return the result.

For more details see [introducing JSX](https://reactjs.org/docs/introducing-jsx.html).

### *rendering elements*
- Elements are the smallest building blocks of React apps.
- An element describes what you want to see on the screen:
  ```json
    const element = <h1>Hello, world</h1>;
  ```
    Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
- Rendering an Element into the DOM:

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element, first pass the DOM element to ReactDOM.createRoot(), then pass the React element to root.render()

- Updating the Rendered Element:

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to root.render().

- React Only Updates What’s Necessary:

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

For more details see [rendering elements](https://reactjs.org/docs/rendering-elements.html).

