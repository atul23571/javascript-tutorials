# Session one

# Overview.

  - Why Javascript ?
  - Defining Variables 
  - Types
  - How to check types ?
  - Objects

# Why JavaScript ?

  - Multipurpose language
  - Easy to understand and start with
  - Can be used write server side as well as client side applications
  -- Web applications
  -- Cross Plateform Mobile applications
  -- Server side applications


# Defining variables
There are three keywords to define varibales in Javascript.
```
$ var <varibalename>;
$ let <varibalename>;
$ const <varibalename>;
```
examples
```
$ var firstName = "Rahul"; // function scope and can be reassigned
$ let lastName = "Singh"; // block scope and can be reassigned
$ const mobile = 9811605039; // block scope and can not be reassigned
```

# Types

JavaScript defines seven built-in data types:
- null
- undefined 
- boolean 
- number
- string 
- object
- symbol //added in es6

### note:
> -> All of these types except object are called "primitives"
> -> Primitives are always assigned/passed by value-copy
> -> Objects always create a copy of the reference on assignment.

# How to check Types ?

```
$ typeof <name of variable>
```
##### example

~~~ 
let firstName; // no value assigned, hence JS assigns undefined by default

typeof firstName; // "undefined" 

firstName = "Rahul";

const age = 30;

let money = null;

let isNonVeg = true;

let address = {
    state: "UP",
    district: "Noida"
}

let favColors = ["red", "blue", "pink"]

function getName(){
    return firstName;
}

typeof money; // "object" // a bug in JS but have to deal with it 
typeof firstName; // "string"
typeof age; // "number"
typeof isNonVeg; // "boolean"
typeof address; // "object"
typeof favColors; // "object" // subtype of object
typeof getName; // "function"


~~~

# Objects

~~~
const obj = {
    name: "Atul Singh",
    email: "atul23571@gmail.com",
    mobile: "9602723622",
    experience: 5,
    age: 28,
    "Knows Javascript ?": true,
    favColors: ['Saffron', 'White', 'Green'],
    address: {
        distt: "New Delhi",
        street: "Chatarpur",
        flat: "1205"
    },
    getAddress() {
        return this.address
    },
    for: 1, //reserved word
    let: 2, // reserved word
    1: "one",
    [{ a: 1 }]: "text"
}

// access
obj.name;   // Atul Singh
obj['name']; // Atul Singh


//check keys if exists
"address" in obj // true
"favFood" in obj // false 

//itterate
for (key in obj) {
    console.log(obj[key])
}
~~~
