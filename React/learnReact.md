# Learning React

## JSX

### Intro to JSX

#### Hello World

`const h1 = <h1>Hello World</h1>;`  
runs in javscript but has HTML syntax

#### What is JSX

syntax extension for Javscript but not valid Javascript, have to compile to run

#### JSX Elements

basic unit of JSX = JSX element  
ex: `<h1>Hello World</h1>`  
HTML syntax

#### JSX Elements and Their Surroundings

JSX elements = Javascript expressions

- can be saved in a variable, passed to a function, stored in object/array

```JSX
const myTeam = {
  center: <li>Benzo Walli</li>,
  powerForward: <li>Rasha Loa</li>,
  smallForward: <li>Tayshaun Dasmoto</li>,
  shootingGuard: <li>Colmar Cumberbatch</li>,
  pointGuard: <li>Femi Billon</li>
};
```

#### Attributes In JSX

JSX can have attributes like HTML and JSX attribute is written using HTML syntax

- a name, followed by an equals sign, followed by a value. The value should be wrapped in quotes
  - `my-attribute-name="my-attribute-value"`

ex:

```JSX
<a href='http://www.example.com'>Welcome to the Web</a>;
const title = <h1 id='title'>Introduction to React.js: Part I</h1>; 
const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px' />;
```

#### Nested JSX

can nest JSX elements inside of other JSX elements  
ex: `<h1>` element nested inside `<a>` element  

``` JSX
const theExample = (
<a href="https://www.example.com">
  <h1>
    Click me!
  </h1>
</a>
)
```

if JSX expression is more than 1 line, must wrap it in parenthesis  
can also be store in a variable

#### JSX Outer Elements

JSX expression must have exactly one outermost element  
this will work

```JSX
const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);
```

but this will not

```JSX
const paragraphs = (
  <p>I am a paragraph.</p> 
  <p>I, too, am a paragraph.</p>
);
```

The first opening tag and the final closing tag of a JSX expression must belong to the same JSX element  
If JSX element has multiple outer elements, just wrap it in `<div></div>`

#### Rendering JSX

```JSX
ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
```

#### `ReactDOM.render()` I

ReactDOM = Javascript library with react-specific methods  
`ReactDOM.render()` - most common way to render JSX

- takes JSX expression, creates a corresponding tree of DOM nodes, and adds that tree to the DOM

1st argument for `ReactDOM.render()` should be a JSX expression

#### `ReactDOM.render()` II

the first argument is appended to whatever element is selected by the second element  
go to `index.hmtl` to find the element that would be selected by `document.getElementbyId('app')`  
the element acted as a containter for `ReactDOM.render()`'s first argument 

```html
<main id="app">
  <h1>Render me!</h1>
</main>
```

changing the id in `index.html` would also require changing the string passed into 2nd argument of `ReactDOM.render()`

#### Passing a Variable to `ReactDOM.render()`

1st argument should evaluate to JSX expression but doesn't have to literally be a JSX expression and can be a variable

```JSX
const toDoList = (
  <ol>
    <li>Learn React</li>
    <li>Become a Developer</li>
  </ol>
);
ReactDOM.render(
  toDoList, 
  document.getElementById('app')
);
```

#### The Virtual DOM

`ReactDOM.render()` only updates DOM elements that have been changed - if you render exact same thing twice in a row, 2nd render won't do anything.  

Virtual DOM is a representation of a DOM object (lightweight copy) - has same properties but lack power to change what's on the screen. Manipulating virtual DOM is fast because nothing is drawn on the screen.

Render a JSX element, every virtual DOM object is updated. After updating, React compares virtual DOM to virtual DOM snapshot taken right before the update. Comparing new DOM w pre-update version - finds out which exact DOM objects have been changed (diffing)

Once React knows which virtual DOM objects have changed, React updates those objects and only those objects on the real DOM - update only necessary parts of DOM

### Advanced JSX


## React Components

### Your First React Component


### Components and Advanced JSX

## Components Interacting

### Components Render Other Components


### this.props


### this.state

## Lifecycle Methods

### Component Lifecycle Methods



## Hooks 

### Function Components


### The State Hook


### The Effect Hook

## Stateless Components From Stateful Components

### Stateless Components From Stateful Components

### Child Components Update Their Parents' state

### Child Components Update Their Siblings' props

## Additional React Basics

### Style

### Containter Components From Presentational Components

### PropTypes

### React Forms 


