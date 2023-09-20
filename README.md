# Calculator NPM Package

## Step 1: Creating your npm account

An npm account is required for publishing an npm package. So make sure you have an npm account before proceeding further.

Creating an npm account is very simple, just follow instructions from this link: [Creating a New npm User Account](https://docs.npmjs.com/creating-a-new-npm-user-account) to create your npm account.

After that, login to your npm via terminal using the following command:
```bash
npm login
```

## Step 2: Creating the package

1. Find a folder on your computer where you would like to keep your project.
2. Create a new folder and name it `calculator`.
3. Open this project inside a terminal and type the following command:

```bash
npm init -y
```

After running the command, a `package.json` file will be created in your `calculator` project folder.

## Step 3: Editing the package.json file

1. Open your project in an Editor.
2. Open your project folder inside an editor.

### Change the name in package.json

1. In the `name` field (this is going to be your package name) of your `package.json`, change it from whatever is the default value (here it is `calculator`) to `@username/calculator`.
2. Replace `@username` with your npm username with `@` as a prefix. For example, if your npm username is `agrim-ani`, then name it as `@agrim-ani/calculator`. Packages with names in this format are called scoped packages.

## Step 4: Create index.js

1. Create a file named `index.js` in your project folder.
2. Add the following code to `index.js`:

```javascript
function add(x, y) { 
    return x + y;
}

function subtract(x, y) { 
    return x - y;
}

function multiply(x, y) { 
    return x * y;
}

function divide(x, y) { 
    return x / y;
}

function remainder(x, y) { 
    return x % y;
}

module.exports = {
    add: add,
    subtract: subtract,
    multiply: multiply,
    divide: divide,
    remainder: remainder
}
```

## Step 5: Publishing your package

Now, we will be publishing this npm package. Open your project folder inside the terminal and type:

```bash
npm publish --access public
```

## Step 6: Testing our npm package

### Create a new folder

1. Create another folder named `test`.

### Initialize it

1. Open the `test` folder inside a terminal and type the following command:

```bash
npm init -y
```

### Install the package

1. After initializing the `test` folder, type the following command in the terminal:

```bash
npm install @agrim-ani/calculator
```

### Create index.js

1. Open the `test` folder inside a code editor and make a new file `index.js`.
2. Type the following code inside `index.js`:

```javascript
const calculator = require('@agrim-ani/calculator');

console.log(calculator.add(1, 1));
console.log(calculator.subtract(6, 7));
console.log(calculator.multiply(2, 4));
console.log(calculator.remainder(6, 3));
console.log(calculator.divide(25, 5));
```
- take help from the images:
  1. install the package
     ![image 1](https://github.com/Agrim-Ani/npm-calculator/blob/main/images/1.png)
  2. write the code
     ![image 2](https://github.com/Agrim-Ani/npm-calculator/blob/main/images/2.png)
  3. test
     ![image 3](https://github.com/Agrim-Ani/npm-calculator/blob/main/images/3.png) 
     

Now, you can test your npm package by running `node index.js` inside the `test` folder.
