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
var goodbye = "Bye Joe";
goodbye = "Goodbye Tony";

console.log(goodbye); //"Goodbye Tony"

```

### <ins> Block scoping rules with `VAR` in non-strict mode </ins>
The variable `VAR` escape from the **block scope**( `generally whenever you see in {curly brackets}` ), at the difference of the function scope  : 

```js
var goodbye = "Bye Joe";
{
  var hello = "Good morning"; // Block Scope 
}

console.log(hello); // "Good morning"

```
