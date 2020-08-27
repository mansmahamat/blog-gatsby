---
title: The difference between Var, Let & Const
author: Mansour Mahamat
date: 2020-08-27
hero: ./images/varletconst.jpeg
excerpt: Setup a project with Tailwind CSS with React JS.
---

With ES6 we have two new ways to create variable , `CONST` and `LET`. These three statements may sound similar, but they have very different uses.

# ~~VAR~~

You can use `VAR` but it's considered bad practice for a junior like me, why ? It can be a source of error in the code.

You can declare `VAR` without assigned value.

`VAR` has a **function scope**,it is available and can be accessed only within that function .

```js
var goodbye = 4; // global scope

function FunctionScope() {
    var hello = 22; // function scope
}

console.log(hello); // Error: hello is not defined
------------------------------------------------------------------

var goodbye = 50; // global scope

function FunctionScope() {
    var hello = 22; // function scope
}

console.log(goodbye); // 50

```

### <ins> Update `VAR` </ins>
We can re-declared and updated the var variables and **it can be a source of errors** if we have big code. We can easily lose our first declarations.

```js
var goodbye;
goodbye = "Goodbye Tony";
goodbye = "Bye John";

console.log(goodbye); //"Bye John"

```

### <ins> Block scoping with `VAR` in non-strict mode </ins>
The variable `VAR` escape from the **block scope**( `generally whenever you see in {curly brackets}` ), at the difference of the function scope  : 

```js
var goodbye = "Bye Joe";
{
  var hello = "Good morning"; // Block Scope 
}

console.log(hello); // "Good morning"

```

# CONST
`CONST` can't be declared without assigned value.

```js
const hello ;
hello = "Hi ! ";

console.log(hello); // Error: Missing initializer in const declaration

```

`CONST` has a **block scope**,it is available and can be accessed only within that block .

```js
const hello = 4; // global scope

 {
    const hello = 22; // block scope
    console.log(hello); // 22
}

console.log(hello); // 4

```

We call this variable `CONST` but it is not always the case like the objects and array :

```js
// Create a const object:
const Pokemon = {name:"Pikachu", type:"Electrique", color:"jaune"};

// Change a property:
Pokemon.color = "Vert";

// Can add a property:
Pokemon.taille = '0,45 m';

console.log(Pokemon); // {name: "Pikachu", type: "Electrique", color: "Vert", taille: "0,45 m"}

------------------------------------------------------------------

// Create a constant array:
const pays = ["France", "Sénégal", "Los Angeles"];

// Change an element:
pays[0] = "Portugal";

// Add an element:
pays.push("Tokyo");

console.log(pays); // ["Portugal", "Sénégal", "Los Angeles", "Tokyo"]

```

But you can't reassign a constant object and array:

```js
const Pokemon = {name:"Pikachu", type:"Electrique", color:"jaune"};
Pokemon = {name:"Bulbizarre", type:"Plante", color:"vert"};
console.log(Pokemon); // Error: Assignment to constant variable.

------------------------------------------------------------------

const pays = ["Mexique", "Brésil", "Australie"];
pays = ["Danemark", "Maroc", "Russie"];
console.log(pays); // Error: Assignment to constant variable.

```

# LET