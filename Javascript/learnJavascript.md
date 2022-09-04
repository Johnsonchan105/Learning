# Learning Javascript for Web Dev

## Introduction

#### Console

To print out values to the console

- `console.log(___)`
  
#### Comments

`// Single line Comments`

``` js
/*
multiline comments
*/
```

#### Data Types

Number  
String  
Boolean  
Null: `null`  
Undefined: `undefined`  
Symbol  
Object  
1st 6 considered primitive data types

#### Arithmetic Operators

+, -, *, /, %

#### String Concatenation

'a string ' + 'sad' gives 'a string sad'

#### Properties

to find the length of a string

- `'Hello'.length` gives 5

#### Methods

`.toUpperCase()` transforms all string to upper case  
`.startsWith(_)` returns true if value inputted is the prefix of string  
`.trim()` removes all whitespace before and after the string

#### Built in Objects

`Math.random()`: gives random number between 0(inclusive) and 1(exclusive)  
`Math.floor(_)`: rounds down the decimal inputted  
`Math.ceil(_)`: rounds up the decimal inputted  
`Number.isInteger(_)`: returns true if value inputted is an integer

- Number object is built in and can find documentation

## Variables

#### Create a Variable: var

Three different types of variables

- `var`
  - declares functionally-scoped or globally scoped variable
- `let`
- `const`

#### Create a Variable: let

`let` signals that the variable can be reassigned with a diferent value
Both `var` and `let`, if not initialized with a value will have a default value of `undefined`

#### Create a Variable: const

`const` variable cannot be reassinged with another value and must be assigned with a value when declared 

##### Self note

- difference between let at var is scoping rules
  - var is scope to immediate function body (function scope)
  - let is scoped to immediate closing block denoted by `{ }` (block scope)

#### Mathematical Assignment Operators

+=, -=, *=, /=

#### Increment and Decrement Operator

++, --

#### String Concatenation with Variables

``` js
let m = 'beans';
console.log('I like ' + m + ' very much');
```

this outputs `I like beans very much`

#### String Interpolation

```js
let m = 'beans';
console.log(`I like ${m} very much`);;
```

this outputs `I like beans very much`  
(note this requires `` instead of '' or "")

#### typeof Operator

check what datatype a variable is

``` js
let m = 'beans';
int i = 1
console.log(typeof m);
console.log(typeof i);
```

this outputs:  

```js
string  
number
```

## Conditionals

#### If... Statments

```js
if(/*boolean statement*/){
    //will run
}else{
    //will run
}
```

#### Comparison Operators

<, >, <=, >=, ===, !==

#### Logical Operators

&&, ||, !

### Truthy and Falsy

Variables are falsy if:

- 0
- Empty Strings like "" or ''
- null - no value at all
- undefined - represent when a declared variable lacks a value
- NaN - not a number

#### Truthy and Falsy Assignment

``` js
let food = 'bean';
let meal = food || 'monkfish';
```

if food is a truthy statement, then it will be assigned to meal, otherwise if it is a falsy statement, meal will be assigned `'monkfish'`

#### Ternary Operator

```js
let aBoolean = true;
aBoolean? statement : anotherstatement;
```

if `aBoolean` is true, then `statement` will be executed, otherwise `anotherstatement` will be executed

#### Switch Statements

```js
let thing = /*something*/;
switch(thing){
  case case1:
    statement1;
    break;
  case case2:
    statement2;
    break;
  default:
    statement3;
    break;
}
```

executes the statement if it hits the case and if nothing hits than executes default.

## Functions

#### Function Declaration

![function declaration form]() // Fix in a bit

#### Calling a Function

Calling a function requires calling the function header `function();`

#### Parameters and Arguments

![function with parameters and arguments](./screenshots/Screen%20Shot%202022-08-26%20at%203.40.59%20PM.png)
![function call and arguments as variables](./screenshots/Screen%20Shot%202022-08-26%20at%203.42.21%20PM.png)

#### Default Parameters

```js
function bonka(var = 'beans'){
  console.log(`I like ${var}`);
}
```

if calling function without a parameter, it will by default use `'beans'`, but if the function is called with a parameter, it will use the inputted parameter instead of `'beans'`

#### Return

![function with return](./screenshots/Screen%20Shot%202022-08-26%20at%203.53.19%20PM.png)

#### Helper Function

meh i know

#### Function Expressions

![Function Expressions Example](./screenshots/Screen%20Shot%202022-08-26%20at%206.25.16%20PM.png)
stores the value of the return for a function into a variable

#### Arrow Function

shorter way to write functions  
replace the function in the function expression

- instead of writing `function` when using function expression instead replace it with `(parameters) =>` 

```js
const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
};
```

#### Concise Body Arrow Functions

![first thing](./screenshots/Screen%20Shot%202022-08-26%20at%206.52.18%20PM.png)

![second thing](./screenshots/Screen%20Shot%202022-08-26%20at%206.53.37%20PM.png)

## Scope

#### Blocks and Scope

code found inside of `{}`

#### Global Scope

variables declared outside of blocks and can use anywhere inside blocks of the same scope 

#### Block Scope

when variable is defined in block, it can only be used in the block and not outside of the paranthesis

#### Scope Pollution

Too many global variables in the global namespace/reuse variables across scopes  
diffficult to keep track of variables and global variables can collide with variables that are locally scoped

## Arrays

#### Arrays

```js
let things = ['a', 1, false];
```

js arrays can store numerous datatypes in a single array.

#### Accessing Elements

know already

#### Update Elements

know already

#### Arrays with `let` and `const`

variables declared with `const` can't be reassigned, but elements in const array still mutable  

arrays created with `let` is any normal array

#### The .length Property

![thing](./screenshots/Screen%20Shot%202022-08-26%20at%207.47.44%20PM.png)

#### The .push() Method

![a](screenshots/Screen%20Shot%202022-08-26%20at%207.48.20%20PM.png)

#### The .pop() Method

![b](screenshots/Screen%20Shot%202022-08-26%20at%207.49.16%20PM.png)

#### More Array Methods

follow link for more array methods: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

#### Arrays and Functions

When passing an array into a functio, if the array is changed within the function, the change will also be maintained on the outside  
Pass by Reference

#### Nested Arrays

2d/3d arrays
`let arr = [[1],[2,3]]`

## Loops

#### The For Loop

```js
for (let i = 0; i < 4; i++){
  /*something*/
}
```

#### The Do-While Statements

loops that runs at least once then loop on specific condition after the initial run

Example:  
![c](screenshots/Screen%20Shot%202022-08-26%20at%207.55.59%20PM.png)

## Iterators

### Higher Order Function

#### Function as Data

can assign functions to variables

```js
let areallylongnameidontknowlol = (a, b) => {
  return a + b;
};
let short = areallylongnameidontknowlol;
console.log(short(1,2)); //will output 
```

functions are a type of object, therefore they will have `.length`, `.name`, and `.toString()` and more properties

#### Functions as Parameters

can pass in functions as parameters into another function

``` js
const func = var => {
  return var * 2;
};
const anotherF = (param, vars) => {
  return p(vars) + vars;
};
console.log(anotherF(func, 2)); 
/*
outputs 6 since the inputted function returns 4 and the higher function add 2 to 4 and returns 6
*/
```

#### The .forEach() Method

![d](screenshots/Screen%20Shot%202022-08-27%20at%2011.38.24%20AM.png)
another method

```js
groceries.forEach(groceryItem => console.log(groceryItem));
//another method
function printGrocery(element){
  console.log(element);
}
groceries.forEach(printGrocery);
```

#### The .map() Method

```js
const numbers = [1,2,3,4,5];
const bigNumbers = numbers.map(number => {return number*10});
//bigNumbers contained [10,20,30,40,50]
```

similar to for each and iterates through the array and returns the modified array

#### The .filter() Method

returns a new array after filtering out certain elements in the original array  
call back function should return `true` or `false` depending on the element passed to it. 

```js
const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door'];
const shortWords = words.filter(w => {
  return w.length < 6;
});
//words will contain all words with less than 6 characters
```

#### The .findIndex() Method

finds the location of an element in an array  
if there is no element that satisfies condition in callback, `.findIndex()` returns -1

```js
const jumbleNums = [123, 25, 78, 5, 9];
const lessThanTen = jumbleNums.findIndex(num => {
  return num < 10;
});
console.log(lessThanTen); // Output: 3 
console.log(jumbledNums[3]); // Output: 5
```

#### The .reduce() Method

returns a single value after iterating through elements of an array

```js
const numbers = [1,2,4,10];
const summedNums = numbers.reduce((accumulator, currentValue)=>{
  return accumulator + currentValue;
}); //summedNums contains 17 after iteration
/*
accumulator:  1| 3| 7
currentValue: 2| 4| 10
return value: 3| 7| 17
*/
```

can also have second parameter that changes the initial value of accumulator

```js
const numbers = [1,2,4,10];
const summedNums = numbers.reduce((accumulator, currentValue)=> {
  return accumulator + currentValue;
}, 100); //<- the second parameter of reduce and accumulator 
         //is now set to 100 and summedNums now contains 117
```

#### Iterator Documentation

documentation contains:  

1. A short definition
2. A block with the correct syntax for using the method
3. A list of parameters the method accepts or requires
4. The return value of the function
5. An extended description
6. Examples of the method's use
7. Other additional information

##### .some()

tests whether at least one element in the array passes the test implemented by the provided function, finds element in the array that returns true and otherwise returns false

```js
const array = [1, 2, 3, 4, 5];
// checks whether an element is even
const even = (element) => element % 2 === 0;
console.log(array.some(even));
// expected output: true
```

#### .every()

tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

```js
const isBelowThreshold = (currentValue) => currentValue < 40;
const array1 = [1, 30, 39, 29, 10, 13];
console.log(array1.every(isBelowThreshold));
// expected output: true
```

## Objects

### Objects

#### Creating Object Literals

use `{}` to define a object literal and creating a object literal is just `let object = {};`  
can fill an object with unordered data organized into key-value pairs  

```js
let spaceship = {
  'Fuel Type' : 'disel', //has quotes because it has space char
  color : 'silver'
};
```

#### Accessing Properties

dot notation

```js
let spaceship = {
  homePlanet: 'Earth',
  color: 'silver'
};
spaceship.homePlanet; // Returns 'Earth',
spaceship.color; // Returns 'silver',
```

if access property not in object, returns undefined

#### Bracket Notation

```js
let spaceship = {
  'Fuel Type': 'Turbo Fuel',
  'Active Duty': true,
  homePlanet: 'Earth',
  numCrew: 5
};
spaceship['Active Duty'];   // Returns true
spaceship['Fuel Type'];   // Returns  'Turbo Fuel'
spaceship['numCrew'];   // Returns 5
spaceship['!!!!!!!!!!!!!!!'];   // Returns undefined
```

MUST use bracket notation when accessing keys that has number, spaces, or special characters  
can use bracket notation  
can use a variable inside bracket to select the keys of an object

```js
let returnAnyProp = (objectName, propName) => objectName[propName];
 
returnAnyProp(spaceship, 'homePlanet'); // Returns 'Earth'
```

#### Property Assignment

1. modifies the property if the property exists within the object
2. adds a new property if the property does not exist within the object

```js
const spaceship = {type: 'shuttle'};
spaceship = {type: 'alien'}; // TypeError: Assignment to constant variable.
spaceship.type = 'alien'; // Changes the value of the type property
spaceship.speed = 'Mach 5'; // Creates a new key of 'speed' with a value of 'Mach 5'
```

cannot reassign object declared in const, but can modify the object and add more within the object itself  
can delete a property using the `delete` operator

```js
const spaceship = {
  'Fuel Type': 'Turbo Fuel',
  homePlanet: 'Earth',
  mission: 'Explore the universe' 
};
delete spaceship.mission;  // Removes the mission property
```

#### Methods

data stored on an object = method  
can include objects in object literals by creating comma-seperated key-value pairs

```js
const alienShip = {
  invade() { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  },
  takeOff() {
    console.log('Spim... Borp... Glix... Blastoff!')
  }
};
```

to call on the method, use `alienShip.invade();` or `alienShip.takeOff()`

#### Nested Objects

object can have objects within them which in turn can have more objects or array of objects  

```js
const spaceship = {
     telescope: {
        yearBuilt: 2018,
        model: '91031-XLT',
        focalLength: 2032 
     },
    crew: {
        captain: { 
            name: 'Sandra', 
            degree: 'Computer Engineering', 
            encourageTeam() { console.log('We got this!') } 
         }
    },
    engine: {
        model: 'Nimbus2000'
     },
     nanoelectronics: {
         computer: {
            terabytes: 100,
            monitors: 'HD'
         },
        'back-up': {
           battery: 'Lithium',
           terabytes: 50
         }
    }
}; 
```

can chain operators to access nested properties  
`spaceship.nanoelectronics['back-up'].battery` returns `'Lithium'`  
array of objects -> `let arr = [{type: 'thing'}];`

#### Pass by Reference

pass a variable assigned to an object into a function as an argument. Functions changing objects that are pass by reference will also change the object itself even when object is assigned to a const variable.

```js
const spaceship = {
  homePlanet : 'Earth',
  color : 'silver'
};
let paintIt = obj => {
  obj.color = 'glorious gold'
};
paintIt(spaceship);
spaceship.color // Returns 'glorious gold'
```

reassignment of the spaceship variable does not work the same

```js
let spaceship = {
  homePlanet : 'Earth',
  color : 'red'
};
let tryReassignment = obj => {
  obj = {
    identified : false, 
    'transport type' : 'flying'
  }
  console.log(obj) // Prints {'identified': false, 'transport type': 'flying'}
};
tryReassignment(spaceship) // The attempt at reassignment does not work.
spaceship // Still returns {homePlanet : 'Earth', color : 'red'};
spaceship = {
  identified : false, 
  'transport type': 'flying'
}; // Regular reassignment still works.
```

#### Looping Through Objects

in order to iterate through objects, use `for...in` syntax  

```js
let spaceship = {
  crew: {
    captain: { 
      name: 'Lily', 
      degree: 'Computer Engineering', 
      cheerTeam() { console.log('You got this!') } 
    },
    'chief officer': { 
      name: 'Dan', 
      degree: 'Aerospace Engineering', 
      agree() { console.log('I agree, captain!') } 
    },
    medic: { 
      name: 'Clementine', 
      degree: 'Physics', 
      announce() { console.log(`Jets on!`) } },
    translator: {
      name: 'Shauna', 
      degree: 'Conservation Science', 
      powerFuel() { console.log('The tank is full!') } 
    }
  }
}; 
// for...in
for (let crewMember in spaceship.crew) {
  console.log(`${crewMember}: ${spaceship.crew[crewMember].name}`);
}
/*
Output:
captain: Lily
chief officer: Dan
medic: Clementine
translator: Shauna
*/
for(let crewMember in spaceship.crew){
  console.log(`${spaceship.crew[crewMember].name}: ${spaceship.crew[crewMember].degree}`);
}
/*
Output:
Lily: Computer Engineering
Dan: Aerospace Engineering
Clementine: Physics
Shauna: Conservation Science
*/
```

### Advanced Objects

#### The this Keyword

references properties created within the object  

```js
const robot = {
  model: '1E78V2',
  energyLevel : 100,
  provideInfo(){
    return `I am ${this.model} and my current energy level is ${this.energyLevel}`
  } 
};
console.log(robot.provideInfo());
//output: I am 1E78V2 and my current energy level is 100
```

#### Arrow Function and this

the arrow function makes `this` calls undefined.

```js
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet: () => {
    console.log(this.dietType);
  }
};
goat.diet(); // Prints undefined
```

AVOID USING ARROW FUNCTIONS WHEN USING `this` IN A METHOD

#### Privacy

convention is to put `_` before the name of a property to mean that the property should not be altered  
similar to private in C++ or Java

#### Getters

methods that get and return interal properties of an object

```js
const person = {
  _firstName: 'John',
  _lastName: 'Doe',
  get fullName() {
    if (this._firstName && this._lastName){
      return `${this._firstName} ${this._lastName}`;
    } else {
      return 'Missing a first name or a last name.';
    }
  }
}
// To call the getter method: 
person.fullName; // 'John Doe'
```

#### Setters

reassign existing values of properties in objects

```js
const person = {
  _age: 37,
  set age(newAge){
    if (typeof newAge === 'number'){
      this._age = newAge;
    } else {
      console.log('You must assign a number to age');
    }
  }
};
person.age = 40;
console.log(person._age); // Logs: 40
person.age = '40'; // Logs: You must assign a number to age
```

#### Factory Functions

create many instance of an object quickly  

```js
const monsterFactory = (name, age, energySource, catchPhrase) => {
  return { 
    name: name,
    age: age, 
    energySource: energySource,
    scare() {
      console.log(catchPhrase);
    } 
  }
};
const ghost = monsterFactory('Ghouly', 251, 'ectoplasm','BOO!');
ghost.scare(); // 'BOO!'
```

#### Property Value Shorthand

new shortcuts for assigning properties to variables called destructuring  

```js
const monsterFactory = (name, age, energySource, catchPhrase) => {
  return { 
    name,
    age,
    energySource,
    scare(){
      console.log(catchPhrase);
    }
  }
};
```

#### Destructured Assignment

extract key-value pairs from objects saved as variables

```js
const vampire = {
  name: 'Dracula',
  residence: 'Transylvania',
  preferences: {
    day: 'stay inside',
    night: 'satisfy appetite'
  }
};
const { residence } = vampire; 
console.log(residence); // Prints 'Transylvania'
const { day } = vampire.preferences; 
console.log(day); // Prints 'stay inside'
```

#### Built in Object Methods

Object instance methods: `.hasOwnProperty`, `.valueOf()`, etc.  

Object class methods: `Object.assign()`, `Object.entries()`, `Object.keys()`, etc  

```js
const robot = {
	model: 'SAL-1000',
  mobile: true,
  sentient: false,
  armor: 'Steel-plated',
  energyLevel: 75
};
```

`Object.keys()` takes an argument and returns all keys for the object in array form  

```js
const robotKeys = Object.keys(robot);
console.log(robotKeys);
/*
Output:
[ 'model', 'mobile', 'sentient', 'armor', 'energyLevel' ]
*/
```

`Object.entries()` takes an argument and returns all key-value pairs in array form  

```js
const robotEntries = Object.entries(robot);
console.log(robotEntries);
/*
Output:
[ [ 'model', 'SAL-1000' ],
  [ 'mobile', true ],
  [ 'sentient', false ],
  [ 'armor', 'Steel-plated' ],
  [ 'energyLevel', 75 ] ]
*/
```

`Object.assign()` takes two arguments, the first being key-value properties to add on to the object, and the second one being the object itself, returns a new object with the added properties.

```js
const newRobot = Object.assign({laserBlaster: true, voiceRecognition: true}, robot);
/*
Output:
{ laserBlaster: true,
  voiceRecognition: true,
  model: 'SAL-1000',
  mobile: true,
  sentient: false,
  armor: 'Steel-plated',
  energyLevel: 75 }
*/
```