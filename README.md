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

<hr>

## Operators in Javascript https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#operator_precedence

1. Arithmetic Operators: + , - ,/ , \* , %, \*\*, ++, --, - , +
   Assignment operator is right associative.
   a = x =20;
   here 20 is assigned to x first and then to a.

2. Comparison: ==, !=, === , !==, < , > , <= , =>
   Here === and == are two different operators in javascript because === means strictly equal and it checks datatype to
   for example 12 == '12' --> true  
   12 === "12" --> false

3. Bitwise Operators: & , |, ^, ~ , << , >>,>>>
4. Logical Operators: && , ||,!
5. Conditional Operators: ? :
6. Comma operator: ,
7. Unary operator: <br/> - delete: to delete any object property<br/> - typeof: return type of object <br/> - void: The void operator specifies an expression to be evaluated without returning a value.
   void expression;
8. Relational Operators: - in: returns true if the specified property is in the specified object <br/> - instanceOf:returns true if the specified object is of the specified object type.
<hr>

## Data types in javascript (Refer Datatypes.js script):

All primitives are immutable. A primitive can be replaced, but it can't be directly altered.
In javascript there are 7 primitive data types.

1. string
2. Number
3. bigint
4. boolean
5. symbol
6. null
7. undefined

## Primitive wrapper objects in JavaScript

Except for null and undefined, all primitive values have object equivalents that wrap around the primitive values:
<b>String</b> for the string primitive.
<b>Number</b> for the number primitive.
<b>BigInt</b> for the bigint primitive.
<b>Boolean</b> for the boolean primitive.
<b>Symbol</b> for the symbol primitive.

The wrapper's valueOf() method returns the primitive value.

## 1. Number

Number is a primitive wrapper object used to represent and manipulate numbers like 37 or -9.25. The Number constructor contains constants and methods for working with numbers. Values of other types can be converted to numbers using the Number() function.
Number in javascript is same as double in java or C#. Its 64 bit

- Number constructor is used to create new Number. Ex. new Number(value)
- Static properties

  1. MAX_SAFE_INTEGER(9007199254740991)
  2. MAX_VALUE(1.7976931348623157e+308): largest positive integer
  3. MIN_SAFE_INTEGER (-9007199254740991)
  4. MIN_VALUE(5e-324) : Smallest positive integer
  5. NaN
  6. NEGATIVE_INFINITY
  7. POSITIVE_INFINITY

- Static method:
  1. Number.isNaN(): Determine whether the passed value is NaN.
  2. Number.isFinite(): Determine whether the passed value is a finite number.
  3. Number.isInteger(): Determine whether the passed value is an integer.
  4. Number.isSafeInteger(): Determine whether the passed value is a safe integer (number between -(2^53 -1) and 2^53 - 1).
  5. Number.parseFloat(string): This is the same as the global parseFloat() function. Number.parseInt(string, [radix]). This is the same as the global parseInt() function.

## 2. String

String is a combination of characters. We can create string by using quotes. String wrapper class is used to manipulate the strings using methods.

1. String(): Constructor is used to create string object using new
   let str = new String("Kajal")

2. Properties:
   length: returns length

3. Methods:

   1. at(index): returns characters present at index, Accepts negative integers, which count back from the last string character.
   2. charAt(index): returns characters present at index
   3. charCodeAt(index): Returns a number that is the UTF-16 code unit value at the given index.
   4. codePointAt(pos): Returns a nonnegative integer Number that is the code point value of the UTF-16 encoded code point starting at the specified pos.
   5. concat(str, [str1, ...]): Combines the text of two (or more) strings and returns a new string.
   6. includes(searchString, pos):Determines whether the calling string contains searchString.
   7. endsWith(searchString, [,position]): Determines whether a string ends with the characters of the string searchString.
   8. indexOf(searchValue, [,fromIndex]):Returns the index within the calling String object of the first occurrence of searchValue, or -1 if not found.
   9. lastIndexOf(searchValue, [,fromIndex]): Returns the index within the calling String object of the last occurrence of searchValue, or -1 if not found.
   10. localeCompare(compareString [, locales [, options]]) Returns a number indicating whether the reference string compareString comes before, after, or is equivalent to the given string in sort order.
   11. match(regexp): Used to match regular expression regexp against a string.
   12. matchAll(regexp): Returns an iterator of all regexp's matches.
   13. normalize([form]): Returns the Unicode Normalization Form of the calling string value.
   14. repeat(count): Returns a string consisting of the elements of the object repeated count times.
   15. replace(searchFor, replaceWith): Used to replace occurrences of searchFor using replaceWith. searchFor may be a string or Regular Expression, and replaceWith may be a string or function.
   16. replaceAll(searchFor, replaceWith): Used to replace all occurrences of searchFor using replaceWith. searchFor may be a string or Regular Expression, and replaceWith may be a string or function.
