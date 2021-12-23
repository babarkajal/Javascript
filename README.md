# Javascript

Javascript Learning

### Day 1 22-12-2021

1. JavaScript is scripting programming language used to give interactivity to static webpages.<br/>
2. HTML defines structure, CSS gives looks to that structure and javascript interactivity.
3. For example: Car which is structure created using some metals, plastic etc (HTML) , Colors design defines its looks and machine working, fuel its motion.
4. A very common use of JavaScript is to dynamically modify HTML and CSS to update a user interface, via the Document Object Model API

How webpage is get loaded inside browser?

1. First browser loads the html page
2. create it's DOM and store it in computer memory
3. Parse CSS and apply to every node
4. Display
5. Load javascript
   https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works/rendering.svg

##### Script loading strategies

When we use inline javascript then it might happen that script gets loaded before HTML parsing. It can create problems. So for this we can use browsers event like <b>DOMContentLoaded</b><br/>
For external scripts <b>defer</b> option is used with script tab which stops execution of code till html get parsed.
async and defer both instruct the browser to download the script(s) in a separate thread, while the rest of the page (the DOM, etc.) is downloading, so the page loading is not blocked during the fetch process.
scripts with an async attribute will execute as soon as the download is complete. This blocks the page and does not guarantee any specific execution order.
scripts with a defer attribute will load in the order they are in and will only execute once everything has finished loading.

https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript/async-defer.jpg

## Operators in Javascript

Arithmetic Operators: + , - ,/ , \* , %
Comparison: === , !==, < , >
Here === and == are two different operators in javascript because === means strictly equal and it checks datatype to
for example 12 == '12' --> true  
12 === "12" --> false

## Variable

Variable is a container which store values.
let a;
when we print a it returns undefined means there is box a which contain nothing. when we address any undeclared variable like
console.log(house); --> house doesn't exit it throws <b color="red">ReferenceError: house is not declared;</b>

Note: Previous js version uses var. Difference between var and let is:

1. Using var we can use variables ahead of its declaration. This is called 'hoisting' Ex.
   log(fruits); //Prints Undefined
   var fruits = "apple"; //Declaration and init
   But Let doesn't allow this behavior.
2. Var declared variable can be used anywhere in the programming regardless of the scope. Let declared variables are limited to block scope only
