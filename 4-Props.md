# Props in React

- Props stands for properties, props are usually passed as argument to a functional component.
- Props are used to pass data from parent to child components, they are readonly and mutabele.

```jsx
function ParentComponent() {
  return <ChildComponent message='Hello, World!' />;
}

function ChildComponent(props) {
  return <p>{props.message}</p>;
}
```

Suppose we create a custom component, we have to add custom props to pass to it, but there is proper validation to check whether the input provided by the user can be right or wrong, to help with that issue react can perform its own validtion using `prop-types`.

1. Install props using `npm install prop-types`.
2. import `import Proptype from 'prop-types'`.

Example:

```jsx
import PropTypes from "prop-types";

const Card = ({ name, age, occupation }) => {
  <div>
    <h1 className='text-lg font-semibold text-white'>{name}</h1>
    <h4 className='text-sm font-semibold text-white'>{age}</h4>
    <h4 className='text-sm font-semibold text-white'>{age}</h4>
  </div>;
};

Card.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number.isRequired,
  occupation: PropTypes.string.isRequired,
};
```

This will validate that the name, age, and occupation props are provided and are of the correct type. If any of these props are missing or of the wrong type, a warning will be displayed in the console during development.

## `Map()` for React

- The `map()` function in React is essential for rendering lists. It simplifies the process by allowing you to return elements directly, without the need for complex loops. This function is commonly used to dynamically generate and display multiple elements, such as list items, from an array of data.
- `map()` in react is the best practice to render a list of elements.

### **Syntax**

`array.map((item, index => {return elements}))`

- The array is what we want to iterate over.
- The `map()` is invoked to the array.
- It takes on or more callbacks as arguments.
- The `item` is the current element in the array.
- The `index` is the current index of the element in the array.
- The `return` is the element that will be rendered.

### **Example**

```js
const fruits = ["Apple", "Banana", "Orange"];

const FruitList = () => (
  <ul>
    {fruits.map((fruit, index) => (
      <li key={index}>{fruit}</li>
    ))}
  </ul>
);

export default FruitList;
```

### **Key Points**

- Alway provide keys in a map function as key's acts as unique identifier for the elements in the array.
- `map()` function returns a new array of elements. usually the an operation is performed on an array, it returns the old array with modified values but `map()` function returns a new array.
- Even if we dont specify the key, react will provide a default key for each element in the array.

### Spread Operator and Uses in React

- The spread operator (...) in JavaScript is a powerful and versatile tool used to expand elements of an iterable (like an array or a string) into individual elements.
- It allows you to copy or merge arrays, pass elements as arguments to functions, and more.
- It is used to copy the existing array into a new array.
- It allows elements of an array to be expaneded into individual elements.
- It can be passed as an argument to a function.
- Helps combining arrays and objects into one without the need of any loops or built-in functions.

#### **Copying Arrays**

```js
const originalArray = [1, 2, 3];
const copiedArray = [...originalArray];
```

### **Why do we need spread operator in react?**

- Immutability: React's state management requires immutability to ensure that components re-render correctly when the state changes. Instead of directly modifying an existing state object or array, the spread operator allows you to create a new copy with the necessary updates.

```js
const newArray = [...oldArray, newItem];
const newObject = { ...oldObject, updatedProperty: newValue };
```

- This approach avoids unintended side effects and bugs that might arise from directly mutating state.
- When merging two objects or arrays into one, it first creates a copy of the first object or array, then it adds the second object or array to the copy. If the properties of both objects or arrays are the same, the second object or array will overwrite the first one.

```js
let todo = {
  id: 3,
  title: "Todo 3",
  description: "Todo 3 description",
};

let newtodo = {
 id: 4,
 title: "Todo 4",
 description: "Todo 4 description"
};

let todos = { ...todo, ...newtodo };
console.log(todos);

Output:
 {
  id: 4,
  title: "Todo 4",
  description: "Todo 4 description"
  };
```

- When you merge two objects into a single array, each object becomes an individual element in the array.
- 