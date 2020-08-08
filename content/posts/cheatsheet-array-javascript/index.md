---
title: Cheatsheet Array Javascript
author: Mansour Mahamat
date: 2020-08-07
hero: ./images/array.jpeg
excerpt: The list of array methods I use most often in JavaScript.
---

### ARRAY LENGTH()
the length () method returns the length of the array.
```javascript
const array = ["hello", "world", "javascript", "array"];
array.length();

4
```

### ARRAY PUSH()
The push () method adds one or more elements to the end of an array and returns the new size of the array.
```javascript
const array = ["hello", "world", "javascript", "array"];
array.push("goodnight");

array = ["hello"," world"," javascript"," array", "goodnight"]
```

### ARRAY POP()
The pop () method removes the last element from an array and returns that element. This method changes the length of the array.
```javascript
const array = ["hello", "world", "javascript", "array"];
array.pop();

array = ["hello"," world"," javascript"," array"]
```

### ARRAY UNSHIFT()
The unshift () method adds one or more elements to the start of an array and returns the new length of the array.
```javascript
const array = ["hello", "world", "javascript", "array"];
array.unshift("code", "everyday")

array = ["code", "everyday", "hello"," world"," javascript"," array"]
```

### ARRAY SHIFT()
The shift () method removes the first element from an array and returns that element. This method changes the length of the array.
```javascript
const array = ["hello", "world", "javascript", "array"];
array.unshift()

array = [" world"," javascript"," array"]
```

### ARRAY FOREACH()
The forEach () method iterates through the array elements one by one to perform a function.
```javascript
const array = ["a", "b", "c", "d"];
array.forEach((element, index) => {
    console.log(`Element ${element} à l'index ${index} </br>`)  
} );

 Element a à l'index 0
 Element b à l'index 1
 Element c à l'index 2
 Element d à l'index 2
```

### ARRAY  FILTER()
The filter () method creates and returns an array containing the elements that check the filter.
```javascript
const array2 = [1, 2, 3, 4, 5];
filter = array2.filter(number => number >= 3);

filter = [3,4,5]
```

### ARRAY MAP()
The map () method returns a new array containing all the elements of the initial array on which the function is called.
```javascript
const array2 = [1, 2, 3, 4, 5];
const map = array2.map(number => number );
const mapWithCondition = array2.map(number => number * 2);

map = [1, 2, 3, 4, 5]
mapWithCondition = [2,4,6,8,10]
```

### ARRAY REDUCE()
La méthode reduce() applique une fonction qui est un « accumulateur » et qui traite chaque valeur d'une liste (de la gauche vers la droite) afin de la réduire à une seule valeur.
```javascript
const array2 = [1, 2, 3, 4, 5];
const reducer = (accumulator, currentValue) => accumulator + currentValue;
const arrayReduce = array2.reduce(reducer );
const arrayReduceWithCondition = array2.reduce(reducer, 100 );

marrayReduce = 15
arrayReduceWithCondition = 115
```

### ARRAY REDUCE()
La méthode slice() renvoie un objet tableau, contenant une copie superficielle (shallow copy) d'une portion du tableau d'origine, la portion est définie par un indice de début et un indice de fin (exclus). Le tableau original ne sera pas modifié.
```javascript
const array = ["hello", "world", "javascript", "array"];
const slice = array.slice(3);

slice = ["javascript", "array"]

```

### ARRAY CONCAT()
La méthode concat() est utilisée afin de fusionner un ou plusieurs tableaux en les concaténant. Cette méthode ne modifie pas les tableaux existants, elle renvoie un nouveau tableau qui est le résultat de l'opération.
```javascript
const array2 = [1, 2, 3, 4, 5];
const array3 = [6, 7, 8, 9, 10];
const arrayConcat = array2.concat(array3);

arrayConcat = [1,2,3,4,5,6,7,8,9,10]

```

### ARRAY JOIN()
La méthode join() crée et renvoie une nouvelle chaîne de caractères en concaténant tous les éléments d'un tableau (ou d'un objet semblable à un tableau). La concaténation utilise la virgule ou une autre chaîne, fournie en argument, comme séparateur.
```javascript
const array2 = [1, 2, 3, 4, 5];
const join = array2.join("-");

arrayConcat = [1-2-3-4-5]

```