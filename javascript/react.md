# Introducing JSX

Consider this:
`const elem = <h1>Hello World!</h1>;`

It is called JSX, a syntax extension to JavaScript. JSX produces react elements.

### Why JSX?
Instead of separating technologies by putting markup and logic in separate files, React separates concern with "components" that contain both. React doesn't require JSX, but it's helpful as a visual aid when working with UI inside JavaScript code.

### Embedding Expressions in JSX
```
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
  
```
