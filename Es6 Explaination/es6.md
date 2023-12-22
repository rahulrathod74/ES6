1.Let and Const keyword and their use cases
The let declaration declares re-assignable, block-scoped local variables, optionally initializing each to a value.

let i=2

2.const
he const declaration declares block-scoped local variables. The value of a constant can't be changed through reassignment using the assignment operator, but if a constant is an object, its properties can be added, updated, or removed.

const name="rahul"
name=sunder
consloe.log("name") //output will be rahul beacuse const constant value can't cahange

3.Arrow function, how it is different from normal function?
Arrow functions in JavaScript are a more concise way of writing functions introduced in ES6. They differ from normal functions (function declarations or expressions) in a few key ways:
arrow function
const add = (a, b) => a + b;

normal function
function add(a, b) {
  return a + b;
}
Arrow Functions: Arrow functions don’t have their own this context. They inherit this from the surrounding code.
Normal Functions: Normal functions have their own this context, which is determined by how they are called.

4.Template literals
Template literals are a feature introduced in ES6 that allow for more flexible and readable string formatting in JavaScript. They're created using backticks (`) instead of single or double quotes. These literals offer several advantages:

const name = 'John';
const age = 30;
const message = `Hello, my name is ${name} and I'm ${age} years old.`;
console.log(message); // Outputs: Hello, my name is John and I'm 30 years old.

5.Default parameters
Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.

function greet(name = 'Guest') {
  console.log(`Hello, ${name}!`);
}

greet(); // Outputs: Hello, Guest!
greet('rahul'); // Outputs: Hello, rahul!

6.for of loop
The for...of loop is a modern iteration construct introduced in ES6 that simplifies the process of iterating over iterable objects like arrays, strings, maps, sets, etc. It provides a more concise and readable way to loop through the elements of an iterable.
const numbers = [1, 2, 3, 4, 5];

for (const num of numbers) {
  console.log(num);
}
// Outputs:
// 1
// 2
// 3
// 4
// 5

7.Object and Array de-structuring 
Object and array destructuring are features introduced in ES6 that allow for easy extraction of values from arrays and properties from objects, respectively, into distinct variables.
*Array Destructuring:
onst numbers = [1, 2, 3, 4, 5];

// Extracting values into variables
const [first, second, ...rest] = numbers;

console.log(first); // Outputs: 1
console.log(second); // Outputs: 2
console.log(rest); // Outputs: [3, 4, 5]

*Object Destructuring
const person = {
  name: 'Alice',
  age: 30,
  city: 'New York'
};

// Extracting properties into variables
const { name, age, city } = person;

console.log(name); // Outputs: Alice
console.log(age); // Outputs: 30
console.log(city); // Outputs: New York

Destructuring provides an elegant and efficient way to extract values from arrays and objects, reducing the need for multiple lines of code to access individual elements or properties. It's widely used in modern JavaScript for cleaner and more expressive code.

8.Rest parameter
The rest parameter syntax allows a function to accept an indefinite number of arguments as an array, providing a way to represent variadic functions in JavaScript.

function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}

console.log(sum(1, 2, 3)); // Outputs: 6
console.log(sum(1, 2, 3, 4, 5)); // Outputs: 15
console.log(sum());

9.Spread operator
he spread operator, introduced in ES6, is denoted by three dots (...). It's a versatile feature used primarily for expanding iterables like arrays, objects, or strings into individual elements or properties.
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const mergedArray = [...arr1, ...arr2];
console.log(mergedArray); // 

10.classes
Classes in JavaScript, introduced in ES6, provide a more convenient and object-oriented way to create blueprints for objects. They offer a cleaner syntax for defining objects and their behavior compared to traditional prototype-based inheritance.

lass Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  greet() {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
  }
}

const alice = new Person('Alice', 25);
alice.greet(); // Outputs: Hello, my name is Alice and I'm 25 years old.