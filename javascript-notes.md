# JavaScript Notes

## 1. Datatypes, Arithmetic & Comparison Operators

JavaScript has multiple datatypes-

- Integer (Whole Number) - Example: `23`, `848`, `347`
- Float (Decimal Number) - Example: `3.14`, `48.938`, `9933.3333`
- String (Textual Data) - Example: `"Hello"`, `"John"`, `"New York"`
- Boolean (True or False) - Example: `true`, `false`
- and more

JavaScript has these operators-

- `+` Addition operator, `10 + 5; // Output: 15`
- `-` Subtraction operator, `10 - 5; // Output: 5`
- `*` Multiplication operator, `10 * 5; // Output: 50`
- `/` Division operator, `10 / 5; // Output: 2`
- `%` Modulus operator, `11 % 5; // Output: 1`
- `==` Comparison (Equality) operator, `11 == 5; // Output: false`
- `!=` Comparison (Equality) operator, `11 != 5; // Output: true`
- `>` Greater than operator, `10 > 5; // Output: true`
- `<` Less than operator, `5 < 10; // Output: true`
- `>=` Greater than equal to operator, `10 >= 5; // Output: true`
- `<=` Less than operator, `5 <= 10; // Output: true`
- `&&` Boolean AND operator, `true && false; // Output: false`
- `||` Boolean OR operator, `true || false; // Output: true`
- `!` Boolean NOT operator, `!true; // Output: false`
- and more

Arithmetic operations can be done as usual-

```js
1 + 1; // Output: 2
0.1 + 0.1; // Output: 0.2
8 - 1; // Output: 7
10 * 2; // Output: 20
35 / 5; // Output: 7
5 / 2; // Output: 2.5
```

Modulo operation can be done using the modulus operator `%`, the mod operation gives the remainder of a division as a result-

```js
10 % 2; // Output: 0
30 % 4; // Output: 2
18.5 % 7; // Output: 4.5
```

Operations can be preferred over one another by using parentheses, the inner most parentheses will be performed on first and then moves towards the outside ones-

```js
(1 + 3) * 2; // Output: 8
3 + 2 * (5 + 10); // Output: 33
```

## 2. Variables

Variables are like boxes, you can store any datatype (Integer, String etc.) inside them.  
Variables are **declared** with the `var` keyword.
Example-

```js
var a;
```

After declaring a variable you can define it by using the `assignment` operator `=`
Example-

```js
a = 20;
```

Thus, there are **two** steps for working with variables-

1. **Declaration** - You are _declaring_ that you'll be working with a variable
2. **Definition** - You are _defining_ the variable by assigning it a value

The values on the _right hand side_ of the assignment sign `=`, is assigned to the box (variable) on the left.

You can declare a variable in a single step, and then define it in another step. Or you can _declare_ and _define_ the variable in a single statement-  
Example-

```js
var a = 10;
```

Anything can be stored inside a variable-  
Example-

```js
var a = 10;
var b = "Hello";
var c = 1.3;
var c = b;
```

Math operations can also be performed on variables if the variables are storing, Integers or Floats-  
Example:

```js
var a = 22;
var b = 7;
var pie = 22 / 7;
```

You can increment (increase) or decrement (decrease) a value inside a variable like this-

```js
var a = 10;
a = a + 1; // a = 10 + 1
```

```js
var a = 10;
a = a + 5; // a = 10 + 5
```

```js
var a = 10;
a = a - 1; // a = 10 - 1
```

There is a shorthand property for incrementing a variable by 1

```js
var a = 10;
a++; // This is same as a = a + 1;
a--; // This is same as a = a - 1;
```

**Note:** You must always use **meaningful** names for variables as it will help you to read, understand and solve bugs in the code later.
Like if you're storing a name inside a variable you must name the variable as `var name = "John";` and **NOT** `var a = "John";`

## 3. Strings

Strings are a list of characters, for example the string `"Hello"` is made up of these individual characters, `H`, `e`, `l`, `l`, `o`.  
**Note:** Strings must be enclosed within single quotes `''` or double quotes `""`, **don't** mix both-  
Example-

```js
var name = "John";
```

The reason we use quotes for strings is because without quotes computer will think it is a variable and try to use it that way, example-

```js
var name = John; // Without quotes John is a variable here.
var name = "John"; // Adding quotes to John makes it a string.
```

You can access indiviual characters of a string by using `bracket notation`, example-

```js
var name = "John";
name[0]; // Output: J
name[1]; // Output: o
name[2]; // Output: h
name[3]; // Output: n
```

Or you can also use the `charAt()` method, example-

```js
var name = "John";
name.charAt(0); // Output: J
name.charAt(1); // Output: o
name.charAt(2); // Output: h
name.charAt(3); // Output: n
```

You can also extract a part of a string also called a **substring**, example-

```js
var message = "Today is a good day.";
message.substring(0, 5); // Output: Today
message.substring(6, 15); // Output: is a good
```

To find out the total number of characters in a string you must use the `length` property, example-

```js
var name = "James Bond";
name.length; // Output: 10
```

To join multiple strings together, we use the `+` operator, example-

```js
var firstName = "James";
var lastName = "Bond";
firstName + " " + lastName; // Output: James Bond
```

### String _Methods_ & _Properties_

There are several Methods and Properties available on Strings, you can use them for various operations, here are a few-

- `length` - This property is used to find out the number of characters in a string, also known as the _length_ of the string, example-

  ```js
  var movie = "Iron Man";
  movie.length; // Output: 8
  ```

- `slice(start, end)` - This methods extracts a part of a string and returns the extracted part as a new string. The method takes 2 parameters: the start position, and the end position (end not included), example-

  ```js
  var college = "Indian Institute of Technology";
  college.slice(7, 16); // Output: Institute
  ```

  If a parameter is negative, the position is counted from the end of the string, example-

  ```js
  var college = "Indian Institute of Technology";
  college.slice(-23, -14); // Output: Institute
  ```

- `substring(start, end)` - This methods extracts a part of a string and returns the extracted part as a new string. The method takes 2 parameters: the start position, and the end position (end not included).  
  `substring()` is similar to `slice()`, the difference is that `substring()` cannot accept negative indexes, example-

  ```js
  var college = "Indian Institute of Technology";
  college.substring(7, 16); // Output: Institute
  ```

- `replace(old, new)` - The `replace()` method replaces a part of a string with a new string, example-

  ```js
  var text = "I am sad";
  text.replace("sad", "happy"); // Output: I am happy
  ```

- `toUpperCase()` - It converts the string to upper case (capital letters), example-

  ```js
  var day = "Friday";
  day.toUpperCase(); // Output: FRIDAY
  ```

- `toLowerCase()` - It converts the string to lower case (small letters), example-
  ```js
  var day = "Friday";
  day.toLowerCase(); // Output: friday
  ```

### Strings are Immutable

Immutable means something **cannot** be modified, whereas mutable means it **can** be modified.
Strings in JavaScript are **Immutable**, therefore when you apply any modification on the string the **original** string is **not** modified, instead a **new** string is returned after applying the modification.

```js
var name = "John";
name[0] = "H"; // You expect the output to be "Hohn", but it will NOT work, because strings are immutable.
```

Similarly, when you use string methods like `slice()`, `substring()`, `replace()`, `toUpperCase()`, etc. to modify a string, the _original_ string is **NOT** modified, instead a **new** string is returned, example-

```js
var day = "Friday";
console.log(day.toUpperCase()); // Output: FRIDAY
console.log(day); // Output: Friday
```

In the above example the _original_ string inside the `day` variable is not modified, it still remains the same.

To update the original string, you have to reassign the modified string to the original variable like this-

```js
var day = "Friday";
day = day.toUpperCase();
console.log(day); // Output: FRIDAY
```

_Note:_ `console.log()` is used for output .

### Escape Characters

You declare strings using either double or single quotes like this-

```js
var name = "John"; // Used Double Quotes ("")
var name = "John"; // Used Single Quotes ('')
```

But when your string contains double quotes, you must use single quotes outside-

```js
var message = 'He said, "I am coming for you".'; // Output: He said, "I am coming for you".
```

And when your string contains single quotes inside, you must use double quotes outside-

```js
var shampoo = "L'Oreal Paris"; // Output: L'Oreal Paris
```

But when your string contains both, double and single quotes, you use a **back slash** `\`, to **escapse** this problem-

```js
var message = 'He said, "I want L\'Oreal Paris shampoo"'; // Output: He said, "I want L'Oreal Paris shampoo"
```

Similarly, when your string contains a back slash, the computer thinks that the back slash is being used for "escaping" purpose and treats it that way, so when you actually want a back slash you add another `\` -

```js
var calc = "2  2"; // Output: 2 2
var calc = "2 \\ 2"; // Output: 2 \ 2
```

Below are the list of **escape characters** and their usage-

| Escape Character | Output |
| ---------------- | ------ |
| \\'              | '      |
| \\"              | "      |
| \\\              | \      |

`\n` and `\t` are few of the escape sequences that are used inside strings for special purposes,example-

- `\n` pushes the string next to it on the **n**ew line
- `\t` adds a TAB

```js
var name = "James\nBond"; /* Output:  James
                                      Bond; */
var name = "James\tBond"; // Output: James  Bond
```

## 4. Comments

Comments are like personal notes and are ignored by the computer, you can write anything in a comment and it will be ignored by the computer.  
They are used to describe what code you're writing, so that anyone understand the code by reading the comments.  
There are 2 types of comments-

- Single Line Comments

  ```js
  // This is a single line comment. By adding 2 forward slashes you comment a single line.
  ```

- Multi Line Comments
  ```js
  /*
        This is a multi line comment.
        To comment multiple lines in a single go, you start the comment with
        a forward slash and a star, and end it with a star and a forward slash.
  */
  ```

This is how a comment is used, to explain code-

```js
/*
    Ask the user for first and last name seperately,
    we can later get the full name by joining the first and last name.
*/
var firstName = "James";
var lastName = "Bond";
var fullName = firstName + " " + lastName; // Adding the first and last name variable to get the full name.
```

## 5. Arrays

Arrays are an **ordered list** of values of **any** data type-  
We declare an array using square brackets `[]`, example-

```js
var myArray = ["James", 40, false];
```

You can declare an empty array like this-

```js
var myArray = [];
```

and then add items to it using bracket notation `[]`-

```js
myArray[0] = "James";
myArray[1] = 40;
myArray[2] = false;
```

Or, you can declare, define and add items to the array at the same time-

```js
var myArray = ["James", 40, false];
```

**Note**: Even though you can store any data type value inside an array.  
For sake of simplicity, always create and use an array containing items (values) of the same type.  
This will prevent many problems and headaches.

This is an _array of **int**_-

```js
var a = [10, 20, 30, 40];
```

An _array of **float**_-

```js
var a = [3.14, 45.23, 76.45, 87.99];
```

An _array of **bool**_-

```js
var a = [true, false, false, true];
```

An _array of **string**_-

```js
var names = ["James", "John", "Jim", "Johnny"];
```

### Accessing an individual item from an Array

You can use bracket notation `[]` to access elements (items) from an array-

```js
var names = ["James", "John", "Jim", "Johnny"];
names[0]; // Output: James
names[1]; // Output: John
names[2]; // Output: Jim
```

### Arrays are mutable

In JavaScript arrays are mutable, meaning the original array can be modified-

```js
var names = ["James", "John", "Jim", "Johnny"];
names[0] = "Julius";
console.log(names); // Output: ["Julius", "John", "Jim", "Johnny"]
```

### Array _Methods_ & _Properties_

There are several Methods and Properties available on Array, you can use them for various operations, here are a few-

- `length` - This property is used to find out the number of elements (items) in an array, also known as the _length_ of the array, example-

  ```js
  var fruits = ["Mango", "Orange", "Apple", "Banana"];
  fruits.length; // Output: 4
  ```

- `push()` - This method adds a new element to the **end** of the array, example-

  ```js
  var fruits = ["Mango", "Orange", "Apple", "Banana"];
  fruits.push("Watermelon");
  console.log(fruits); // Output: ["Mango", "Orange", "Apple", "Banana", "Watermelon"]
  ```

- `pop()` - This method removes an element from the **end** of the array, example-

  ```js
  var fruits = ["Mango", "Orange", "Apple", "Banana"];
  fruits.pop();
  console.log(fruits); // Output: ["Mango", "Orange", "Apple"]
  ```

- `shift()` - This method removes the first element from the front/start of the array, example-

  ```js
  var fruits = ["Mango", "Orange", "Apple", "Banana"];
  fruits.shift();
  console.log(fruits); // Output: ["Orange", "Apple", "Banana"]
  ```

- `unshift()` - This method adds an element at the front/start of the array, example-

  ```js
  var fruits = ["Mango", "Orange", "Apple", "Banana"];
  fruits.unshift("Watermelon");
  console.log(fruits); // Output: ["Watermelon", "Mango", "Orange", "Apple", "Banana"]
  ```

### Why and when to use array?

When you want to represent **similar** items or a list in your code, you must use arrays.
For example, you can use multiple string variables to store a list of animals like this-

```js
var tiger = "Tiger";
var lion = "Lion";
var giraffe = "Giraffe";
var jaguar = "Jaguar";
var elephant = "Elephant";
var zebra = "Zebra";

console.log(tiger, lion, giraffe, jaguar, elephant, zebra);
```

But it is difficult to manage them, you have to again and again create a new variable, also you cannot find out how many animals are there.

A better way is to use an array to store them like these-

```js
var animals = ["Tiger", "Lion", "Giraffe", "Jaguar", "Elephant", "Zebra"];
console.log(animals);
console.log("I have " + animals.length + " animals"); // Output: I have 6 animals.
```

### Single and Multi Dimensional Arrays

You've seen single dimensional arrays-

```js
var animals = ["Tiger", "Lion", "Zebra"];
animals[0]; // Output: Tiger
```

When you put one array inside another array, you get a 2D array (multidimensional array)-

```js
var pets = ["Cat", "Rabbit", "Dog"];
var animals = [pets];
```

The above code can be written in short like this-

```js
var animals = [["Cat", "Rabbit", "Dog"]];
```

Note than we have a single array on the outside, and then another array as it's first element.  
You can use double brackets notation to access 2D array (multidimensional)-

```js
var animals = [["Cat", "Rabbit", "Dog"]];
animals[0]; // Output: ["Cat", "Rabbit", "Dog"]
animals.length; // Output: 1
animals[0][0]; // Output: Cat
animals[0][1]; // Output: Rabbit
animals[0][2]; // Output: Dog
animals[0].length; // Output: 3
```

You can keep adding arrays inside arrays and keep going to create, 1D, 2D, 3D, 4D, 5D, nD arrays.

## 6. Conditions

Conditional statements are used to perform different actions based on different conditions or decisions.
In JavaScript we have the following conditional statements-

- Use `if` to specify a block of code to be executed, if a specified condition is true
- Use `else` to specify a block of code to be executed, if the same condition is false
- Use `else if` to specify a new condition to test, if the first condition is false
- Use `switch` to specify many alternative blocks of code to be executed

### `if` statement

You use the `if` statement to execute a code if a condition is `true`-
Syntax-

```js
if (condition) {
  //  block of code to be executed if the condition is true
}
```

Example-

```js
if (day == "Sunday") {
  console.log("Holiday!");
}
```

### `else` statement

You use the `else` statement to execute a code if a condition is `false`-
Syntax-

```js
if (condition) {
  //  block of code to be executed if the condition is true
} else {
  //  block of code to be executed if the condition is false
}
```

Example-

```js
if (day == "Sunday") {
  console.log("Holiday!");
} else {
  console.log("Working Day");
}
```

### `else if` statement

You use the `else if` statement to specify a new condition if the first condition is `false`-
Syntax-

```js
if (condition1) {
  //  block of code to be executed if condition1 is true
} else if (condition2) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
```

Example-

```js
if (day == "Sunday") {
  console.log("Holiday!");
} else if (day == "Saturday") {
  console.log("Holiday!");
} else {
  console.log("Working Day");
}
```

You can have multiple `else if` statements to specify multiple conditions, example-

```js
if (day == "Sunday") {
  console.log("Holiday!");
} else if (day == "Saturday") {
  console.log("Holiday!");
} else if (day == "Independence Day") {
  console.log("Holiday!");
} else {
  console.log("Working Day");
}
```

Multiple conditions can be chained together using boolean operators `&&` (Boolean AND), and `||` (Boolean OR), example-

```js
if (day == "Sunday" || day == "Saturday" || day == "Independence Day") {
  console.log("Holiday!");
} else {
  console.log("Working Day");
}
```

```js
if (mood == "happy" && day == "Sunday") {
  console.log("No work, only fun! :)");
} else {
  console.log("Sad life :(");
}
```

### `switch` statement

The `switch` statement is used to perform different actions based on different conditions. It is similar to `if else`.

When you have a large `if else` code like below, it becomes difficult to manage it-

```js
if (day == "Monday") {
  console.log("Work");
} else if (day == "Tuesday") {
  console.log("Work");
} else if (day == "Wednesday") {
  console.log("Work");
} else if (day == "Thursday") {
  console.log("Work");
} else if (day == "Friday") {
  console.log("Work");
} else if (day == "Saturday") {
  console.log("Chill");
} else if (day == "Sunday") {
  console.log("Chill");
} else {
  console.log("The day is wrong");
}
```

We use a `switch` statement in such scenarios-

```js
switch (day) {
  case "Monday":
    console.log("Work");
    break;
  case "Tuesday":
    console.log("Work");
    break;
  case "Wednesday":
    console.log("Work");
    break;
  case "Thursday":
    console.log("Work");
    break;
  case "Friday":
    console.log("Work");
    break;
  case "Saturday":
    console.log("Chill");
    break;
  case "Sunday":
    console.log("Chill");
    break;
  default:
    console.log("The day is wrong");
}
```

Note: If you don't specify the `break` keyword, JavaScript will keep comparing all the `cases` till the end. By specifying `break` we are exiting the `switch` code block as soon as one condition matches.
Note: The `default` keyword specifies the code to run if there is no case match, it is like the `else` statement.

## 7. Loops

Loops execute a block of code a specified number of times. Loops are used, if you want to run the same code again and again, each time with a same or different value.

### The `for` loop

Syntax-

```js
for (initial; condition; operation) {
  // code block to be executed
}
```

The `for` loop has three constructs-

1. initial - The `for` loop starts with this initial value.
2. condition - The `for` loop checks this condition at every loop/run/iteration.
3. operation - At the end of every single loop it performs this operation.

Example-

```js
for (var i = 0; i < 3; i++) {
  console.log(i);
}
```

The above for loop has these three constructs-

- initial - It starts with a variable `i` having value `0`
- condition - At every iteration it checks if the value of `i` is less than `3`
- operation - After every iteration it increments (increases) the value of `i` by `1`

#### Using `for` loop to access all the elements of an array

You can access all the elements of an array manually like this-

```js
var animals = ["Tiger", "Lion", "Zebra"];
animals[0];
animals[1];
animals[2];
```

But this way it is very hectic, imagine if the array has hundreds, thousands, or millions of elements.
This is where looping shines, you can use `for` loop to do the same task, example-

```js
var animals = ["Tiger", "Lion", "Zebra"];
for (var i = 0; i < animals.length; i++) {
  animals[i];
}
```

## 8. Functions

A function is a block of code designed to perform a specific task.
A function is defined with the `function` keyword, followed by a name, followed by brackets/parentheses ().

The code to be executed, by the function, is placed inside curly brackets: {}

Syntax-

```js
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

Functions are used in two step-

1. Defining a function-
   ```js
   function name(parameter1, parameter2, parameter3) {
     // code to be executed
   }
   ```
2. Calling it

   ```js
   name(argument1, argument2, argument3);
   ```

Example-

```js
// We first define the function.
function add(a, b) {
  var result = a + b;
  return result;
}
```

```js
// Calling the function.
add(1, 2); // Output: 3
```

_Note_: You must **define** a function **before** **using** it.

### Function Parameters & Arguments

#### **Parameters**

When you define a function, you specify the parameters that the function will accept as input-

```js
function double(n) {
  var result = n * 2;
  return result;
}
```

In the above `double()` function, the variable `n` is an input parameter, you can specify as many input parameters as required in the function definition seperated by a comma, example-

```js
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

If you don't require any parameters you shouldn't specify any parameter in the function definition-

```js
function name() {
  // code to be executed
}
```

#### **Arguments**

Arguments are the actual values passed to the function while calling it, example-

```js
function multiply(a, b) {
  var result = a * b;
  return result;
}

multiply(2, 5);
```

Here, in the function **definition** the variables `a` and `b` are **parameters**.  
Whereas while calling the function we **pass** the actual values `2` and `5`, and these are **arguments**.  
So, the parameters `a` and `b`, receive the arguments `2` and `5`.

**Note: Difference between parameters and arguments-**  
Function parameters are the names listed in the function's definition.  
Function arguments are the real values passed to the function while calling it.

#### **Return** value of a function

When JavaScript reaches a `return` statement, the function will **stop** executing and _return_ immediately.

If the function was invoked from a statement, JavaScript will _return_ to execute the code after the invoking statement.

Functions return their output through a `return` value. The return value is "returned" back to the "caller" of the function, example-

```js
// This function accepts two parameters (inputs) a and b.
function multiply(a, b) {
  var result = a * b;
  return result; // This function returns (output) the product of a and b.
}

var x = multiply(2, 4); // The function is called from here, so the return value (output) will be stored in x.
```

<!--
## 6. Objects

You have many things around you - Car, Book, Phone, House, Watch, etc.
Objects in JavaScript are used to represent such real life things (objects).
Every object has two things-

1. Properties - Properties are the features or qualities of the object
2. Methods - Methods are the behaviours or the functionalities of the object

Example-

| Object | Properties                          | Methods                           |
| ------ | ----------------------------------- | --------------------------------- |
| Car    | Brand, Model, Color, Variant, Price | Start, Drive, Brake, Stop         |
| Book   | Name, Author, Category, Price       | Open, Turn Page, Bookmark,Close   |
| Watch  | Brand, Model, Color, Price          | Start Tick, Stop Tick, Play Sound |
-->
