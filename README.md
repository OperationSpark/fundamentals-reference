# Table of Contents
HTML & CSS
HTML
CSS
Variables and Data
Variables
Simple / Primitive Data Types
Strings
Numbers
Booleans
Complex Data Types
Arrays
Objects
Operators
Arithmetic Operators: + - / * %
Comparison Operators: > < >= <= !== ===
Assignment Operators: = += -= *= /= %=
Constructs
Functions
Creating New Functions
Using (Calling) Functions
Conditional Statements:
if statements
else statements
else if statements
Loops
Repeat code N times: Using for loops
Repeat code until...: Using while loops
Iteration
Iterating over Arrays using a for loop.
Iterating over Objects using a for in loop.

# HTML & CSS

## HTML and `.html` files
HTML stands for **H**yper**t**ext **M**arkup **L**anguage and is responsible for defining the **structure and content** of a website. 

To create a new website, we create new `.html` files. HTML files can be created in any text editor. Typically a home page will be created with the name `index.html`. 

Every `.html` file starts with the HTML code below:

```html
<DOCTYPE !HTML>
<html>
  <head>
    <!-- Meta Data -->
  </head>
  <body>
    <!-- Content: Pictures, Links, Headers, Text, etc... -->
  </body>
</html>
```

### Elements and HTML Tags
HTML websites are created using tags. An HTML tag consists of pair of `< >` with the *type* of content that you want to add. Some examples of different types of tags are:

```html
<h1> This is a header: size 1</h1>
<p> This is a paragraph </p>
<a href="operationspark.org> This is a link to Operation Spark's website </a>
```


Most tags require both an *opening* and *closing* tag. Closing tags are written: `</ >` with the type of the element inside. The three pairs of tags above each create content that will be displayed to the user. The text that is written between the two tags is what the user sees while the tags themselves will be hidden.

### Structure Tags and Element Nesting
Each tag serves a specific purpose. Some tags add content to a page that the user sees. Other tags are used to provide structure and organization to the website. 

For example, the `<body> </body>` tags in the `index.html` template are used to contain all visible content. If we were to include the header, paragraph, and link from the previous example in our website, we would add it between the opening and closing tags of the `body` like so:

```html
<body>
  <!-- Content: Pictures, Links, Headers, Text, etc... -->
  <h1> This is a header: size 1</h1>
  <p> This is a paragraph </p>
  <a href="operationspark.org"> This is a link to Operation Spark's website </a>
</body>
```

Within the `body` of our website, we can create even more subsections using the `<div> </div>` tags.

Suppose you wanted to have a navigation bar at the top of your page, a section in the middle for content, and a footer at the bottom. The HTML for this website might look like this:

```html
<body>
  <!-- Content: Pictures, Links, Headers, Text, etc... -->
  <div id="navigation-bar"> 
    <a href="operationspark.org"> This is a link to Operation Spark's website </a>
  </div> 
  
  <div id="main-content">
    <h1> This is a header: size 1</h1>
    <p> This is a paragraph </p>
  </div>
  
  <div id="footer"> 
    <p> This is the footer paragraph </p>
  </div>
</body>
```

When we place an HTML tag inside another, this is called **Nesting**. To keep our code organized, nested HTML tags are indented from their "parent" tags. 

### Attributes
Attributes are additional pieces of data attached to an HTML tag. Examples include
- The path to the location of an image file 
- A URL for a link
- Classes and IDs

Attributes are written inside the opening tag of an element. 

```html
<a href = "google.com"> take me to Google! </a>
<img src = "pictures/icons/hallebot-pic.jpg">
<div id = "main-content">
  <h1> This is a header: size 1</h1>
  <p> This is a paragraph </p>
</div>
```
**Classes and IDs**
`class` and `id` are attributes that can be given to any HTML tag to identify them and/or group them.
This is useful for CSS styling purposes, DOM access, and much more. See the CSS section for how to use IDs and Classes for grouped styling:


CSS
CSS stands for Cascading Style Sheets and is responsible for defining the style of a webpage. It is written as a series of style-based rules for which HTML elements should follow (ex: all paragraphs should be red and have arial font). CSS style blocks can be written directly within an HTML file between <style> tags or in a separate .css file. 

Style Block
A collection of style rules that a specific HTML tag (or set of HTML tags) should follow. They require a selector, {curly braces}, and properties.

selector {
  property-name: property-value;
}


This example sets the rule: all paragraphs should be red and use arial font:

p {
  color: red;
  font: arial;
}

CSS Property
Properties are the various ways in which we can style HTML elements. They are written with the name of the property, the desired value, and end with a semicolon.

color: red;


There are hundreds of properties and values to choose from. Google is your friend.


CSS Selector
The selector determines which HTML tags will be styled. Selectors can be:
The name of a HTML tag
An id attribute name written as #id
A class attribute name written as .class 
This example sets the rule: all tags with the class="mainText" attribute will have a background color of blue and all tags with the id="headline" attribute will have font-size of 28 pixels and be black.

.mainText {
  background-color: blue;
}

#headline {
  font-size: 28px;
  color: black;
}
  	
Variables and Data

There are only a few types of data in JavaScript which fall into two categories: simple data types and complex data types. Every type of data can be stored in a variable. 
Variables
A variable is a named container for data.
The var keyword declares a new variable with a variableName
The variable is assigned a value using the = operator. 
Variables only need to be declared once but can be re-assigned many times. 
Referencing the name of the variable will return the value it contains.

var variableName = "some data";	    => variableName returns "some data"
Simple / Primitive Data Types
Simple / primitive data types represent a single value. 

Strings
A collection of characters / symbols surrounded by quotes (" " or ' '). 
Strings can be combined using the + operator
Strings have a length property which returns the number of characters in the string

var name = "ben";
var phrase = "hello " + name;	   => phrase returns "hello ben"
var phraseLength = phrase.length;  => phraseLength returns 9


Numbers
Any numerical value: positive, negative, or with decimal points
Numbers can be created with arithmetic expressions

var age = 17;				   => age returns 17  
var sum = (age + 3) * 10;		   => sum returns 200 
 
Booleans
A true or false value. Typically used in conditional statements.
Booleans can be created with boolean expressions using comparison operators
Comparison Operators are: >, >=, <, <=, === (equal), !== (not equal)

var canDrive = true;
var bool = (sum === 200);  		=> bool returns true
var canVote = (age >= 18);  		=> canVote returns false
Complex Data Types
Complex Data Types represent a collection of values. They can contain ANY type of data, simple or complex. Each piece of data is stored at a particular position in the collection (at an index for Arrays, at a key for Objects).

Arrays
Arrays are collections of data in an ordered list.
Array values are stored in square brackets separated by commas: [ ]
var myArray = ['a', 'b', 'c'];


Arrays are Zero-Indexed.  Every element (data value) has an index: the numerical position of the value in the list. The first value in the list has an index of 0 and each index after increases by 1.


Bracket notation accesses / modifies the value in the array at the index provided:
var firstValue = myArray[0];	⇒ firstValue = 'a';
myArray[2] = 'd';			⇒ assigns index 2 to 'd'
						⇒ myArray = ['a', 'b', 'd'];

myArray.length property returns the number of elements currently in myArray. 
var arrayLength = myArray.length;	⇒ arrayLength = 3


Arrays have a .push() method (and more) that adds a value to the end of the Array. 
myArray.push('e');	⇒ myArray = ['a', 'b', 'd', 'e']


Example: Storing your day's schedule as a list of activities

var schedule = ['math', 'english', 'spanish', 'physics', 'band'];
var firstPeriod = schedule[0];		=> firstPeriod is math
var thirdPeriod = schedule[2];		=> thirdPeriod is spanish

// dropping physics and taking up history
schedule[3] = 'history';	

var numberOfClasses = schedule.length;	=> numberOfClasses is 5

// adding afterschool activities
schedule.push('soccer practice');
schedule.push('tutoring');




Objects
Objects are collections of data that describe a single entity:
Object values are stored in curly braces { }. Every value has a key that it is paired with. Each key:value pair is called a property.
var myObject = { 
  key1: 'a', 
  key2: 'b',
  key3: 'c'  
};


Access/Update Object values with Dot Notation:
var myValue = myObject.key1; 	⇒ myValue = 'a'
myObject.key1 = 'apple'; 		⇒ reassigns key1 to apple


Access/Update Object values with Bracket Notation. When using bracket notation the key must be written as a string and this is typically done using a variable: 
var myKey = "key1";
var myValue = myObject[myKey]; 	⇒ myValue = 'a'
myObject[myKey] = 'apple';		⇒ reassigns key1 to apple


Objects don't have a .length property.

Example: Storing all information about a single user in an Object

var user = { 
name: "John", 
age: 25, 
isAdmin: false 
};

var userName = user.name;			=> userName = "John"
var userAge = user.age;			=> userAge = 25
user.age = 26;					=> userAge = 26
var newAge = user["age"];			=> newAge = 26
user.isAdmin = true;				=> changes isAdmin to true
user["isAdmin"] = false;			=> changes isAdmin to false

Operators
Operators act on data (operands) to produce new data values.

Arithmetic Operators: + - / * % 
Used to perform Mathematical operations
Return Numbers (the + operator can be used on Strings however)

var sum = 4 + 5;		=> sum = 9
var diff = 4 - 5;		=> diff = -1
var quotient = 4 / 5;		=> quotient = 0.8
var product = 4 * 5;		=> product = 20;
var remainder = 4 % 5;	=> remainder = 4

Comparison Operators: > < >= <= !== ===
Used to compare any two values
Return Booleans
The === and !== operators should always be used instead of == or !=

var lessThan = 4 < 5;			  => lessThan = true
var lessThanOrEqual = 4 <= 5;	  => lessThanOrEqual = true
var greaterThan = 4 > 5;		  => greaterThan = false
var greaterThanOrEqual = 4 >= 5;	  => greaterThanOrEqual = false
var equalTo = 4 === 5;	  	  => equalTo = false
var notEqualTo = 4 !== 5;	  	  => notEqualTo = true

Assignment Operators: = += -= *= /= %=
Used to assign new values to variables
Return the value provided for assignment
The = operator can be combined with Arithmetic operators

var number = 5;			=> number = 5
number += 1;			=> number = number + 1 = 6
number *= 2;			=> number = number * 2 = 12
number /= 4;			=> number = number / 4 = 3
number %= 2;			=> number = number % 2 = 1




Constructs
Functions
Functions are reusable blocks of code that execute a sequence. The can accept inputs and return a new data value. 

There are two phases to Functions: declaring functions and calling functions


Creating New Functions
The basic syntax for creating a function looks like this:


function <functionName>(<param1>, <param2>) {
  // code to be reused
}


Parameters (<param1>, <param2>)are variables that reference the inputs to a function when the function is called.
The function's {code block} defines the code to be executed when the function is called.
The return keyword (see example below) determines what value is returned to the caller of the function when the function is called.
The example function below accepts two number inputs and returns their sum.


function add(num1, num2) {
  var sum = num1 + num2;
  return sum;
}

Using (Calling) Functions 
A Function Call is how we command a function to execute its code and return a value. It looks like this: <functionName>(<argument1>, <argument2>)
Arguments are specific input values to be used by the function when making a function call.
The function call will return a value which may be assigned to a variable.

var result1 = add(2, 3);				=> result1 returns 5
var result2 = add(result1, 5);			=> result2 returns 10
var result3 = add(result1, result2);		=> result3 returns 15

Conditional Statements: 
Often times, programs will need to perform some action conditionally, meaning the action will occur only IF some condition is true. For example, GMail.com will only allow you to view your emails IF you enter your password correctly. Consider the variables below:

var age = 25, isAdmin = false;

if statements
Runs a {code block} only if a condition is true. 
The condition can be any boolean value ( true / false ) or any boolean expression using a comparison operator. The condition MUST be inside (parentheses). 

if (age >= 18) {
	// code to allow user to access mature content
}

else statements
MUST follow an if statement
else statements DO NOT have a condition of their own. 
Runs a {code block} only if the previous condition is false. 

if (isAdmin) {
	// code to allow user to access administrative content
} else {
	// code to deny user access to all content
}


else if statements
MUST follow an if (could be another else if statement)
else if statements are else statements with a condition. 
Runs a {code block} only if the previous condition is false and its own condition is true.

if (isAdmin) {
	// code to allow user to access administrative content
} else if (age >= 18) {
	// code to allow user to access mature content
} else {
	// code to deny user access to all content
}

Loops
Loops allow us to repeat some code multiple times. When creating loops to repeat our code, it is helpful to think about 3 questions: 1) What do you want to repeat? 2) What changes from loop to loop? 3) How long will the loop run?

Repeat code until...: Using while loops
while loops repeatedly execute a block of code while some condition remains true.
The condition is a boolean expression wrapped in parentheses ( ). The value of the expression is checked before each loop . If the condition is  true the loop will continue. If it is false the loop will break.
Below is an example of a loop increases the value of age by 1 until it equals 18.

var age = 0;
while (age < 18) {
	age = age + 1;
}
console.log("you can now vote!");


Repeat code N times: Using for loops
for loops use a counting variable to repeat code a specific number of times.
They require three statements wrapped in( parentheses ) and separated by semicolons. (see below for example)


The start statement: declare the counting variable i and set its starting value. We use this variable track how many loops have been performed. 
The stop condition is written as a boolean expression whose value is checked before each loop. While this expression is true the loop will repeat execution.
The update statement changes the value of the counting variable after each loop so that eventually the stop condition is false. Failure to do so can result in infinite loops!


Below is an example of a loop that runs 10 times and prints:
	"loop #1", "loop #2", "loop #3"..., "loop #10"

    start     stop     update
for (var i = 1; i <= 10; i = i + 1) {
	console.log("loop #" + i);
}





Iteration
Iteration is the process of accessing values in a Collection using a loop. 

Iterating over Arrays using a for loop.
The counting variable i will count all indexes in the Array starting at 0.
The stop condition: i < arr.length will make the loop run once for each index in the array, stopping after the last index ( i = arr.length - 1 )
Inside the loop, we use bracket notation: arr[i] to access each value in the Array. The value accessed by arr[i] change as the value of i changes on each loop.

for (var i = 0; i < arr.length; i = i + 1) {
var eachValue = arr[i]
// code to repeat using eachValue and/or i
}

This example iterates over the nums Array and prints each value doubled


// indexes:  0,  1,  2,  3,  4
var nums = [10, 20, 30, 40, 50];
for (var i = 0; i < nums.length; i = i + 1) {
var eachNum = nums[i];
console.log(eachNum * 2);
}

Iterating over Objects using a for in loop.
for in loops are loop designed specifically to iterate over the properties of Objects
The variable key is assigned to each key of the obj Object on each loop. 
To access the values along the way we use bracket notation: obj[key]. The each value accessed by obj[key] will change as the value of key changes.

for (var eachKey in obj) {
var eachValue = obj[key]
// code to do something with each key and/or value
}

This example iterates over the grades Object and adds 10 to every grade


var grades = {english: 75, math: 80, spanish: 83};
for (var key in grades) {
var eachGrade = grades[key];
grades[key] = (eachGrade + 10);
}
// grades = {english: 85, math: 90, spanish: 93};

