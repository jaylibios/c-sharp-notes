# 2. Introducing JSX

Consider this:
`const elem = <h1>Hello World!</h1>;`

It is called JSX, a syntax extension to JavaScript. JSX produces react elements.

### Why JSX?
Instead of separating technologies by putting markup and logic in separate files, React separates concern with "components" that contain both. React doesn't require JSX, but it's helpful as a visual aid when working with UI inside JavaScript code.

### Embedding Expressions in JSX
```javascript
const name = "Josh Perez";
const elem = <h1>Hello { name }!</h1>;

ReactDOM.render(
  elem,
  document.getElementById("root")
);
```

In the exmaple below, we embed the result of calling a function into an `<h1>` element.
  
```
function formatName(user) {
  return user.firstName + " " + user.lastName;
}

const user = {
  firstName: "Harper",
  lastName: "Perez"
};

const element = (
  <h1> Hello, { formatName(user) }!</h1>
);

reactDOM.render(
  elem,
  document.getElementById("root");
);
  
```

**TIP: Since JSX is cloer to JavaScript than to HTML, React DOM uses camelCase naming instead of HTML attribute names.
E.g `class` becomes `className` in JSX, and `tabindex` becomes `tabIndex`.**

### Specifying Children with JSX
If a tag is empty, you can immediately close it like XML:
` const elem = <img src={ user.avatarUrl } />`

JSX tags may contain children:
```
const elem = (
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you.</h2>
  </div>
);
```

### JSX Prevents Injection Attacks
It's safe to embed user input:
```
const title = response.potentiallyMaliciousInput;
// This is safe:
const elem = <h1>{ title }</h2>
```

By default, React DOM escapes any valyes embedded in JSX before rendering. This ensures you can never inject anything not explicitly written in the application. Everything is converted to a string before being rendered, preventing XSS (cross-site-scripting) attacks.

### JSX Represents Objects
Babel compiles JSX down to `React.createElement()` calls.
These two are identical:
1.
```
const elem = (
  <h1 className="greeting">Hello, World!</h1>
);
```

2.
```
const elem = React.createElement(
  "h1",
  { className: "greeting" },
  "Hello, World!"
);
```

These objects are called "React elements". Think of them as descriptiong of what you want to see on the screen.

----------

# 3. Rendering Elements
An element describes what you want to see.
`const element = <h1>Hello, world!</h1>`
Unlike browser DOM elements, React elements are plain objects and cheap. Elements are not components. Elements are what components are "made of" (components are composed of elements).

### Rendering an Element into the DOM
In the HTML file, there is a `<div>`
`<div id="root"></div>`

We call this a "root" DOM node b/c everything inside will be managed by React DOM.

To render a React element into a root DOM node, pass both to `ReactDOM.render()`;
```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById("root"));
```

### Updating the Rendered Element
React elements are immutable; once you create the element, its children and attributes cannot be changed. The only way to update the UI is to create a new element and pass it to the `ReactDOM.render()`.

Consider this example:
```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is { new Date().toLocaleTimeString() }</h2>
    </div>
  );
  
  ReactDOM.render(element, root);
}

setInterval(tick, 1000);
```
If calls `ReactDOM.render()` every second from a `setInterval()` callback.

### React Only Updates What's Necessary
React DOM only applies updates necessary to bring the DOM to desired state.

Even though we created an element describing the whole UI tree on every tick, only the text node whose contents changed gets updated by React DOM.

----------

# Components and Props
