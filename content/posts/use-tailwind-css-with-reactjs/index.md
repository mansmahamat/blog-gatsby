---
title: How use Tailwind CSS with React JS
author: Mansour Mahamat
date: 2020-08-08
hero: ./images/tailwind.png
excerpt: Setup a project with Tailwind CSS with React JS.
---

### TAILWIND CSS ?
Tailwind is a highly customizable CSS framework with which you can quickly create your own web pages and components. Different classes exist and we can create our own classes so as not to repeat an element that we use a lot of times.
```jsx
<p className="text-purple-700 text-opacity-100">Hello World ...</p>
```
[Un lien vers la documentation](https://tailwindcss.com/) to know more.

#### Create React App
```git
npx create-react-app demo
cd demo
```

#### Install Tailwind CSS
```git
npm install tailwindcss postcss-cli autoprefixer -D
```
The command below will create a tailwind.js file with all the properties of Tailwind (color, margin ...), this file will allow us to write our Tailwind classes : 
```git
npx tailwind init tailwind.js --full
```

#### Configure Post CSS
Create a file postcss.config with this command : 
```git
touch postcss.config.js
```

Inside postcss.config.js paste this line :
```git
const tailwindcss = require('tailwindcss');
module.exports = {
    plugins: [
        tailwindcss('./tailwind.js'),
        require('autoprefixer')
    ],
};
```