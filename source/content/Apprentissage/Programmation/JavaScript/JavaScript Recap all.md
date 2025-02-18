

```js
var myName = "Beau"; //var => going to be use throughtout whole program 
let ourName = "freeCodeCamp"; //let =>  a variable with the same name can only be declared once and can only be use within the scope of where you declared it
const pi = 3.14; //const => variable that can't never change +feature of let.

var theName;
/* peut contenir $ et _
et déclater sans donner valeur ou type.*/

//MATH !
i--; // == i = i - 1
i++; // == i = i + 1 

a = i % t // a = reste de la division 

myVar += 5; // myVar = myVar + 5;
myVar -= 5; //soustraction
myVar *= 5; //multiplication
myVar /= 5; // myVar = myVar / 5;
```

##### Global vs Local Scope in Functions

```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}

myFun() 
//The function `myFun` will return the string `Head` because the local version of the variable is present.
```
###### Global Scope
In JavaScript, scope refers to the visibility of variables. 
Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.
Variables which are declared without the `let` or `const` keywords are automatically created in the `global` scope.


###### Local Scope
Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.
Hence if call outside the function, (like when calling the function) -> give an error.


#### Strings 
```js
//pour que les guillements s'affiche
const sampleStr = "Alan said, \"Peter is learning JavaScript\".";

const a = "texte" //same as
const b = 'texte aussi' //this allow to do
const conversation = 'Finn exclaims to Jake, "Algebraic!"'; //sans les '\'


//pour rajouter "I come second" a 'ourStr'
let ourStr = "I come first. ";
ourStr += "I come second.";
//ou, on peut additionner de même les Strings
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;

//constuire des String avec des variables
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";


//length of a string, sort 10
console.log("Alan Peter".length);


//bracket notation; give "C"
const firstName = "Charles";
const firstLetter = firstName[0];

//Find the Last Character in a String
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
```


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



#### Arrays <=> Tableau

```js
const sandwich = ["peanut butter", "jelly", "bread"];

//Multidimensional array
const teams = [["Bulls", 23], ["White Sox", 45]];


const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];
const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
/*`subarray` has the value `[[10, 11, 12], 13, 14]`, 
`nestedSubarray` has the value `[10, 11, 12]`, and `element` has the value `11`*/

//Modifier Array
const ourArray = [50, 40, 30];
ourArray[0] = 15;

//ajouter un élément a la fin d'un array
	ourArray[-1] = 2;

```


##### Push, pop, shift, unshift
```js
//PUSH()
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
/*`arr1` now has the value `[1, 2, 3, 4]` and `arr2` has the value `["Stimpson", "J", "cat", ["happy", "joy"]]`. */


//POP(): removes the last element from an array and returns that element.
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
/*The first `console.log` will display the value `6`,
and the second will display the value `[1, 4]`.*/

//shift() removes the first element and store it somewhere else. 
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
//'removedFromOurArray` would have a value of the string `Stimpson`, and `ourArray` would have `["J", ["cat"]]`.


//unshift() add element at the begining of the Array
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
//`ourArray` would have the value `["Happy", "J", "cat"]`.
```

##### Nested Arrays
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



#### Function

```js
// Assignment with a Returned Value
let processed = 0;
function processArg(num) {
  return (num + 3) / 5;
}
processed = processArg(7)


//Undefined Value returned, no use of 'return'
let sum = 0;
function addSum(num) {
  sum = sum + num;
}
addSum(3); //return 6 but the value is undefined. 
```


#### IF Statement
```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}

/*Logical Order in If Else Statements
The function is executed from top to bottom 
so you will want to be careful of what statement comes first.*/
```

##### Type Coercion allow different data type to be compare: 
```js
1   ==  1  // true
1   ==  2  // false
1   == '1' // true
"3" ==  3  // true
```

###### Strict equality (`===`)
```js
3 ===  3  // true
3 === '3' // false
```

 ##### Inequality Operator
```js
1 !=  2    // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
```

###### Strict Inequality Operator
```js
3 !==  3  // false
3 !== '3' // true
4 !==  3  // true
```

##### And / Or Operators
(`||`) returns `true` if either of the operands is `true`. Otherwise, it returns `false`.
```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
// return `Yes`  if `num` is between `5` and `10` (5 and 10 included). 
```

#### Switch Statements

```js
switch (lowercaseLetter) {
  case "a":               //`case` values are tested with strict equality (`===`).
    console.log("A");
    break;
  case "b":
    console.log("B");
    break; /*The `break` tells JavaScript to stop executing statements. If the `break` is omitted, the next statement will be executed. */
  default:  /*will be executed if no matching 'case' statements are found */
	 defaultStatement; 
	break;


//Multiple Identical Options
let result = "";
switch (val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";

}
```


#### Object

```js
const anotherObject = {
  make: "Peace", 
  5: "five", //if your object has any non-string properties, JavaScript will automatically typecast them as strings.
  "model": "focus",
  "Space Name": "Kirk",
  "NoSpace": "USS Enterprise"
};

//two ways to access the properties of an object:
//dot notation (`.`) 
//and bracket notation (`[]`), similar to an array.
const valeur = anotherObject.make;
const autreValeur = anotherObject["Space Name"];

/*Another use of bracket notation on objects is to access a property which is stored as the value of a variable.*/
const monModel = "Mantra";
const a = anotherObject[monModel];
consol.log(a); //display "focus"

//to update the "make":
anotherObject.make = "Marijuana legal";
//or 
anotherObject["make"] = "Marijuana legal";

//add a property to the Object:
anotherObject.poisson = "crue";
//or
anotherObject["poisson"] = "crue";

//to delede the property
delete anotherObject.poisson;

//Testing object for property: check if the property of a given object exists or not.

anotherObject.hasOwnProperty("make"); //return true
anotherObject.hasOwnProperty("poisson"); // return false
//can do
if (anotherObject[make].hasOwnProperty("tracks") === false){
	anotherObject["poisson"] = "crue";
}
```


###### Accessing object properties with variables
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

##### Complex Objects

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

###### Nested Objects
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
