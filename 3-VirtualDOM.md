# Virtual DOM in React

_**Document Object Model**_

- The Document Object Model (DOM) is a programming interface that represents the structure of a webpage as a tree of objects. Each element, attribute, and piece of text in the HTML document is represented as a node in this tree structure. The DOM allows programs and scripts to dynamically access and update the content, structure, and style of a document.

Representation of DOM:

```html
<div id="container">
  <h1>Hello, World!</h1>
  <p>This is a paragraph.</p>
</div>
```

- Tree like representation:

```html
- Document - HTML - BODY - DIV (id="container") - H1 - P
```

_**Virutal DOM**_

- The Virtual DOM is a lightweight copy of the actual DOM. It is a programming abstraction that represents the structure of a web page in memory. The Virtual DOM is used to optimize the rendering process by minimizing direct manipulation of the actual DOM, which can be expensive in terms of performance.
