#javascript 
https://www.youtube.com/watch?app=desktop&v=PkZNo7MFNFg&feature=youtu.be&fbclid=IwAR2nqC6tMKeCLWwm5jeQ5gVkQPjtsyZ49Qhf3YCjmrvQvFb1aWQJKuuwk5w

https://www.freecodecamp.org/learn


###### Running JavaScript
- sublime text
create htlm file

###### Comment Your Code
```js
var number = 5; //in line comment
/* this is a 
multi-line comment*/
```

#### Declare Variables
7 data type:
- string
- number
- undefined 
	- variable non set
- null
	- variable nul ou nothing
- boolean
	- true or false
- symbol
	- immuable primitiva value that is unique
- object
	- store a lot of different key value pairs

###### déclarer une variable: 

```js
var myName = "Beau"; //peut contenir $ et _
let ourName = "freeCodeCamp";
const pi = 3.14;
```

peut déclarer aussi sans donner la valeur / data typ: 
```js
var theName;
```

###### différence 
var => going to be use throughtout whole program

let =>  a variable with the same name can only be declared once and can only be use within the scope of where you declared it

const => variable that can't never change +feature of let. 


**Note:** It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays


#### Increment and Decrement
```js
i--;
i++;
```

#### Decimal Numbers
We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.


#### Finding a Remainder
The remainder operator `%` gives the remainder of the division of two numbers.

**Note:** The remainder operator is sometimes incorrectly referred to as the modulus operator. It is very similar to modulus, but does not work properly with negative numbers.


#### Augmented Math Operations

```js
myVar = myVar + 5;
myVar += 5; //version augmenter
myVar -= 5; //soustraction
myVar *= 5; //multiplication
myVar /= 5;

```


#### Declare String Variables
use " " ou ' ' pour déclarer String.

#### Escaping Literal Quotes
you can escape a quote from considering it as an end of string quote by placing a backslash (`\`) in front of the quote.

```js
const sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```

#### Quoting Strings with Single Quotes
single and double quotes work the same in JavaScript.
The reason why you might want to use one type of quote over the other is if you want to use both in a string. This might happen if you want to save a conversation in a string and have the conversation in quotes. Another use for it would be saving an `<a>` tag with various attributes in quotes, all within a string.

```js
const conversation = 'Finn exclaims to Jake, "Algebraic!"';
const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
//both are correct
```


#### Escape Sequences
Quotes are not the only characters that can be escaped inside a string. There are two reasons to use escaping characters:

1.  To allow you to use characters you may not otherwise be able to type out, such as a newline.
2.  To allow you to represent multiple quotes in a string without JavaScript misinterpreting what you mean.

Code|Output
--|--
`\'`|single quote
`\"`|double quote
`\\`|backslash
`\n`|newline
`\t`|tab
`\r`|carriage return
`\b`|word boundary
`\f`|form feed


#### Plus Equals Operator
We can also use the `+=` operator to concatenate a string onto the end of an existing string variable. This can be very helpful to break a long string over several lines

```js
let ourStr = "I come first. ";
ourStr += "I come second.";
```

#### Constructing Strings with Variables
```js
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";
```

#### Appending Variables to Strings
```js
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;
```

#### Length of a String
```js
console.log("Alan Peter".length);
//sort 10
```


#### Bracket Notation
Bracket notation is a way to get a character at a specific index within a string.
Most language start counting at 0 vs human at 1. 

```js
const firstName = "Charles";
const firstLetter = firstName[0];
//give "C"
```

##### Understand String Immutability
```js
let myStr = "Bob";
myStr[0] = "J";
//=> give error, the right code is:
let myStr = "Bob";
myStr = "Job";

```

###### Use Bracket Notation to Find the Last Character in a String
```js
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
//give "a"
```

#### Arrays
```js
const sandwich = ["peanut butter", "jelly", "bread"];
```

##### Nest Arrays - multi-dimensional array
```js
const teams = [["Bulls", 23], ["White Sox", 45]];
```

##### Access Array Data
```js
const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];
//The `console.log(array[0])` prints `50`, and `data` has the value `60`.
```

##### Modify Array Data
```js
const ourArray = [50, 40, 30];
ourArray[0] = 15;
	```

##### Access Multi-Dimensional Arrays
```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

In this example, `subarray` has the value `[[10, 11, 12], 13, 14]`, `nestedSubarray` has the value `[10, 11, 12]`, and `element` has the value `11`

##### push()
An easy way to append data to the end of an array is via the `push()` function.
`.push()` takes one or more parameters and "pushes" them onto the end of the array.

```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

`arr1` now has the value `[1, 2, 3, 4]` and `arr2` has the value `["Stimpson", "J", "cat", ["happy", "joy"]]`.

##### pop()
`.pop()` is used to pop a value off of the end of an array. We can store this popped off value by assigning it to a variable. In other words, `.pop()` removes the last element from an array and returns that element.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```

The first `console.log` will display the value `6`, and the second will display the value `[1, 4]`.

##### shift()
`pop()` always removes the last element of an array. What if you want to remove the first?


That's where `.shift()` comes in. It works just like `.pop()`, except it removes the first element instead of the last and store it somewhere else. 

```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```

`removedFromOurArray` would have a value of the string `Stimpson`, and `ourArray` would have `["J", ["cat"]]`.

#### unshift() 
`unshift` elements to the beginning of an array i.e. add elements in front of the array.
`.unshift()` works exactly like `.push()`, but instead of adding the element at the end of the array, `unshift()` adds the element at the beginning of the array.

```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```
`ourArray` would have the value `["Happy", "J", "cat"]`.


#### Write Reusable code with Functions

```js
function reusableFunction(){
  console.log("Hi World");
}
reusableFunction();
```

##### Arguments
```js
function functionWithArgs(argument1,argument2){
  console.log(argument1 + argument2);
}
functionWithArgs(2 + 3);
//give 5
```

###### Return
```js
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
```

#### Global Scope
In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.
Variables which are declared without the `let` or `const` keywords are automatically created in the `global` scope.


#### Local Scope
Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.
Hence if call outside the function, (like when calling the function) -> give an error.

#### Global vs Local Scope in Functions
```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}

myFun() 
//The function `myFun` will return the string `Head` because the local version of the variable is present.
```


#### Return a Value from a Function
##### Undefined Value returned
A function can include the `return` statement but it does not have to. In the case that the function doesn't have a `return` statement, when you call it, the function processes the inner code but the returned value is `undefined`.

```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}
addSum(3);
```

`addSum` is a function without a `return` statement. The function will change the global `sum` variable but the returned value of the function is `undefined`.

##### Assignment with a Returned Value

```js
// Setup
let processed = 0;
function processArg(num) {
  return (num + 3) / 5;
}
// Only change code below this line
processed = processArg(7)
```


###### Stand in Line
In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.



#### Boolean Values
Another data type is the Boolean. Booleans may only be one of two values: `true` or `false`. They are basically little on-off switches, where `true` is on and `false` is off. These two states are mutually exclusive.


##### If Statements
`if` statements are used to make decisions in code. The keyword `if` tells JavaScript to execute the code in the curly braces under certain conditions, defined in the parentheses. These conditions are known as `Boolean` conditions and they may only be `true` or `false`.

```js
function test (myCondition) {
  if (myCondition) {
    return "It was true";
  }
  return "It was false";
}

test(true);
test(false);
```

`test(true)` returns the string `It was true`, and `test(false)` returns the string `It was false`.


##### Equality Operators
```js
function equalityTest(myVal) {
  if (myVal == 10) {
    return "Equal";
  }
  return "Not Equal";
}
```


Type Coercion allow different data type to be compare: 
```js
1   ==  1  // true
1   ==  2  // false
1   == '1' // true
"3" ==  3  // true
```


However Strict equality (`===`) is the counterpart to the equality operator (`==`). However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

```js
3 ===  3  // true
3 === '3' // false
```

###### Comparison with the Inequality Operator
The inequality operator (`!=`) is the opposite of the equality operator. It means not equal and returns `false` where equality would return `true` and _vice versa_. Like the equality operator, the inequality operator will convert data types of values while comparing.

```js
1 !=  2    // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
```

###### Comparison with the Strict Inequality Operator

The strict inequality operator (`!==`) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns `false` where strict equality would return `true` and _vice versa_. The strict inequality operator will not convert data types.

```js
3 !==  3  // false
3 !== '3' // true
4 !==  3  // true
```

##### And / Or Operators
The logical or operator (`||`) returns `true` if either of the operands is `true`. Otherwise, it returns `false`.

The logical or operator is composed of two pipe symbols: (`||`).

```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
```

will return `Yes` only if `num` is between `5` and `10` (5 and 10 included). 


##### Else Statements

```js
if (num > 10) {
  return "Bigger than 10";
} else {
  return "10 or Less";
}
```

##### Else If Statements 
```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

#### Logical Order in If Else Statements
The function is executed from top to bottom so you will want to be careful of what statement comes first.


#### Switch Statements

```js
switch (lowercaseLetter) {
  case "a":
    console.log("A");
    break;
  case "b":
    console.log("B");
    break;
}
```

`case` values are tested with strict equality (`===`). The `break` tells JavaScript to stop executing statements. If the `break` is omitted, the next statement will be executed.

##### Default statement
In a `switch` statement you may not be able to specify all possible values as `case` statements. Instead, you can add the `default` statement which will be executed if no matching `case` statements are found. Think of it like the final `else` statement in an `if/else` chain.

A `default` statement should be the last case.

```js
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  default:
    defaultStatement;
    break;
}
```

##### Multiple Identical Options in Switch Statements
If the `break` statement is omitted from a `switch` statement's `case`, the following `case` statement(s) are executed until a `break` is encountered. If you have multiple inputs with the same output, you can represent them in a `switch` statement like this:

```js
let result = "";
switch (val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
```


#### Returning Boolean Values from Functions

instead of
```js
function isEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}
```

Do:

```js
function isEqual(a, b) {
  return a === b;
}
```


#### Return Early Pattern for Functions
When a `return` statement is reached, the execution of the current function stops and control returns to the calling location.

```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```

The above will display the string `Hello` in the console, and return the string `World`. The string `byebye` will never display in the console, because the function exits at the `return` statement.

#### Build Objects
```js
const cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```

In this example, all the properties are stored as strings, such as `name`, `legs`, and `tails`. However, you can also use numbers as properties. You can even omit the quotes for single-word string properties, as follows:

```js
const anotherObject = {
  make: "Ford",
  5: "five",
  "model": "focus"
};
```

However, if your object has any non-string properties, JavaScript will automatically typecast them as strings.

There are two ways to access the properties of an object: dot notation (`.`) and bracket notation (`[]`), similar to an array.

##### Dot Notation
Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

```js
const myObj = {
  prop1: "val1",
  prop2: "val2"
};

const prop1val = myObj.prop1;
const prop2val = myObj.prop2;
```

`prop1val` would have a value of the string `val1`, and `prop2val` would have a value of the string `val2`.

##### Bracket Notation
If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

 ```js
const myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  "NoSpace": "USS Enterprise"
};

myObj["Space Name"];
myObj['More Space'];
myObj["NoSpace"];
```


##### Accessing Object Properties with Variables
Another use of bracket notation on objects is to access a property which is stored as the value of a variable. This can be very useful for iterating through an object's properties or when accessing a lookup table.

```js
const dogs = {
  Fido: "Mutt",
  Hunter: "Doberman",
  Snoopie: "Beagle"
};

const myDog = "Hunter";
const myBreed = dogs[myDog];
console.log(myBreed);

//The string `Doberman` would be displayed in the console.
```


#### Updating Object Properties 
```js
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

//to update the "name" of "ourDog":
ourDog.name = "Happy Camper";
//or 
ourDog["name"] = "Happy Camper";


//Here's how we would add a `bark` property to `ourDog`:
ourDog.bark = "bow-wow";
//or
ourDog["bark"] = "bow-wow";

//to delede "bark" property
delete ourDog.bark;

```
Can use Objects instead of a break !


##### Testing Objects for Properties
Sometimes it is useful to check if the property of a given object exists or not. We can use the `.hasOwnProperty(propname)` method of objects to determine if that object has the given property name. `.hasOwnProperty()` returns `true` or `false` if the property is found or not.

```js
const myObj = {
  top: "hat",
  bottom: "pants"
};

myObj.hasOwnProperty("top");
myObj.hasOwnProperty("middle");
```

The first `hasOwnProperty` returns `true`, while the second returns `false`.




#### Manipulating Complex Objects

```js
const myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  },
  
  {
    artist: "Deep Purple",
    title: "Smoke on the water",
    release_year: 1976,
    formats: ["CD", "8T", "LP"]
  }
];
```


#### Nested Objects
The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

Here is a nested object:

```js
const ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};

ourStorage.cabinet["top drawer"].folder2;
ourStorage.desk.drawer;
```

`ourStorage.cabinet["top drawer"].folder2` would be the string `secrets`, and `ourStorage.desk.drawer` would be the string `stapler`


#### Nested Arrays
```js
const ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];

ourPets[0].names[1];
ourPets[1].names[0];
```

`ourPets[0].names[1]` would be the string `Fluffy`, 
and `ourPets[1].names[0]` would be the string `Spot`.


#### Record Collection
- [ ] exo a refaire 
You start with an `updateRecords` function that takes an object literal, `records`, containing the musical album collection, an `id`, a `prop` (like `artist` or `tracks`), and a `value`. Complete the function using the rules below to modify the object passed to the function.

-   Your function must always return the entire record collection object.
-   If `prop` isn't `tracks` and `value` isn't an empty string, update or set that album's `prop` to `value`.
-   If `prop` is `tracks` but the album doesn't have a `tracks` property, create an empty array and add `value` to it.
-   If `prop` is `tracks` and `value` isn't an empty string, add `value` to the end of the album's existing `tracks` array.
-   If `value` is an empty string, delete the given `prop` property from the album.


```js
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  if (prop !== "tracks" && value !== "") {
    records[id][prop] = value;
} else if (prop === "tracks" && value !== "" && records[id].hasOwnProperty("tracks") === false) {
    records[id][prop] = [value];

  } else if (prop === "tracks" && value !== "") {
    records[id][prop].push(value);

  } else if (value === "") {
    delete records[id][prop];
  }
  return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');
```


#### Loops
##### While Loops
```js
const ourArray = [];
let i = 0;

while (i < 5) {
  ourArray.push(i);
  i++;
}
```

##### For Loops
For loops are declared with three optional expressions separated by semicolons:

`for (a; b; c)`, where `a` is the initialization statement, `b` is the condition statement, and `c` is the final expression.

```js
const ourArray = [];

for (let i = 0; i < 5; i++) {
  ourArray.push(i);
}
```
`ourArray` will now have the value `[0, 1, 2, 3, 4]`.

##### Odd Numbers With a For Loop
```js
const ourArray = [];

for (let i = 0; i < 10; i += 2) {
  ourArray.push(i);
}
```

`ourArray` will now contain `[0, 2, 4, 6, 8]`.



##### Iterate Through an Array with a For Loop
```js
const arr = [10, 9, 8, 7, 6];

for (let i = 0; i < arr.length; i++) {
   console.log(arr[i]);
}
```

Remember that arrays have zero-based indexing, which means the last index of the array is `length - 1`. 
Our condition for this loop is `i < arr.length`, which stops the loop when `i` is equal to `length`. 
In this case the last iteration is `i === 4` i.e. 
when `i` becomes equal to `arr.length - 1` and outputs `6` to the console. Then `i` increases to `5`, and the loop terminates because `i < arr.length` is `false`.


##### Nesting For Loops 
```js
const arr = [
  [1, 2], [3, 4], [5, 6]
];

for (let i = 0; i < arr.length; i++) {
  for (let j = 0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

This outputs each sub-element in `arr` one at a time. Note that for the inner loop, we are checking the `.length` of `arr[i]`, since `arr[i]` is itself an array.


##### Do...While Loops
```js
const ourArray = [];
let i = 0;

do {
  ourArray.push(i);
  i++;
} while (i < 5);
```


#### Replace Loops using Recursion
Recursion is the concept that a function can be expressed in terms of itself.

Example: multiply the first `n` elements of an array to create the product of those elements. Using a `for` loop, you could do this:
```js
 function multiply(arr, n) {
    let product = 1;
    for (let i = 0; i < n; i++) {
      product *= arr[i];
    }
    return product;
  }
```


However, notice that `multiply(arr, n) == multiply(arr, n - 1) * arr[n - 1]`. That means you can rewrite `multiply` in terms of itself and never need to use a loop.
```js
function multiply(arr, n) {
    if (n <= 0) {
      return 1;
    } else {
      return multiply(arr, n - 1) * arr[n - 1];
    }
  }
```



#### Random Fractions and Whole Numbers
JavaScript has a `Math.random()` function that generates a random decimal number between `0` (inclusive) and `1` (exclusive). Thus `Math.random()` can return a `0` but never return a `1`.


###### to generate random whole numbers
1.  Use `Math.random()` to generate a random decimal.
2.  Multiply that random decimal by `20`.
3.  Use another function, `Math.floor()` to round the number down to its nearest whole number.

Remember that `Math.random()` can never quite return a `1` and, because we're rounding down, it's impossible to actually get `20`. This technique will give us a whole number between `0` and `19`.

Putting everything together, this is what our code looks like:

```js
Math.floor(Math.random() * 20);
```


#### parseInt Function
#### Ternary Operator
#### Multiple Ternary Operators
#### var vs let
#### const Keyword
#### Mutate an Array Declared with const
#### Prevent Object Mutation
#### Arrow Functions
#### Default Parameters
#### Rest Operator
#### Spread Operator
#### Destructuring Assignment
#### Template Literals
#### Simple Fields
#### Declarative Functions
#### class Syntax
#### getters and setters
#### import and export