# React

It is a state management library, that is used in building user interface.

React allows devs to create re-useabele UI components which improves code organisation and maintainability.

_React uses a virtual DOM to optimize rendering_. It updates only the parts of the DOM that have changed, which enhances performance and provides a smoother user experience by reducing unnecessary re-renders.

## Component Hierarchy

- **Parent and Child Components**: React applications often consist of nested components. The parent component usually contains and manages the state, and it must be exported using the `export default` keyword to be used by other components.

- **Inheritance of Properties**: Child components can inherit properties (props) from their parent component. However, when a state is passed down from the parent, it may cause the parent component to re-render every time the state changes.

- To group and return multiple elements, without adding extra nodes to the DOM. We wrap multiple elements in one fragament `<></>`, we can also use `<div></div>`

- if using inline css to style jsx elements, we specify the style in `style = {{}}`. Specify the style inside the curly braces.

- To render a list of componets, we use the `map()` function.
- Use of ternary operator makes the code look clearner. `condition ? "True" : "False`.

### What is babel, what does it exactly do

- Babel is a transpiler, that enabeles developers to write modern ES6 JavaScript and JSX, it enables compatability with a wide range of browsers, including old and latest.

- Babel makes sure that the JavaScript we write, works in all environments.
- Babel is responsible for converting the JSX code to JavaScript code that all browsers understand.
