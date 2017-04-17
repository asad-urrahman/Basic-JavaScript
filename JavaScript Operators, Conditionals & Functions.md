# JavaScript Operators, Conditionals & Functions



It is essential to have a firm grasp of the fundamentals before delving into creating programs with JavaScript. In this article, we will go over some of the most important basic concepts of JavaScript that will allow you to start writing your own programs: operators, conditional statements, and functions.



### Table of Contents  



*   [JavaScript Operators](#javascriptoperators)
*   [Assignment Operators](#assignmentoperators)
*   [Arithmetic Operators](#arithmeticoperators)
*   [Addition](#addition)
*   [Subtraction](#subtraction)
*   [Multiplication](#multiplication)
*   [Division](#division)
*   [Modulus](#modulus)
*   [Increment](#increment)
*   [Decrement](#decrement)
*   [Comparison Operators](#comparisonoperators)
*   [Equal](#equal)
*   [Strict Equal](#strictequal)
*   [Not Equal](#notequal)
*   [Strict Not Equal](#strictnotequal)
*   [Less Than](#lessthan)
*   [Less Than or Equal To](#lessthanorequalto)
*   [Greater Than](#greaterthan)
*   [Greater Than or Equal To](#greaterthanorequalto)
*   [Logical Operators](#logicaloperators)
*   [And](#and)
*   [Or](#or)
*   [Not](#not)
*   [Operator Precedence](#operatorprecedence)
*   [Conditional Statements](#conditionalstatements)
*   [If / Else](#ifelse)
*   [If](#if)
*   [Else](#else)
*   [Else If](#elseif)
*   [Switch](#switch)
*   [Functions](#functions)
*   [Declaration](#declaration)
*   [Invocation](#invocation)
*   [Parameters and Arguments](#parametersandarguments)
*   [Conclusion](#conclusion)



Before we begin, you should have an understanding of basic JavaScript syntax, comments, data types, and assigning values to variables. You can learn or review all that information in [A Beginner’s Guide to JavaScript Variables and Data Types](https://www.sitepoint.com/beginners-guide-javascript-variables-and-datatypes/).

> **Disclaimer:** This guide is intended for complete beginners to JavaScript and programming. As such, many concepts will be presented in a simplified manner, and strict ES5 syntax will be used.

Ready? Let’s get started!



## JavaScript Operators

JavaScript **operators** are symbols that are used to perform different operations on data. There are several types of operators in JavaScript, and in this lesson we’ll learn about the most common ones: assignment operators, arithmetic operators, comparison operators, and logical operators.

### Assignment Operators

**Assignment operators**, in their most basic form, apply data to a variable. In this example, I’ll assign the string `"Europe"` to the variable `continent`.

    var continent = "Europe";

Assignment is represented by the equals sign (`=`). Although there are other types of assignment operators, which [you can view here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators), this is by far the most common.

You can test all the examples throughout this article by using the `console.log()` function, or by [using the Console](https://developers.google.com/web/tools/chrome-devtools/console/).

### Arithmetic Operators

JavaScript, like all programming languages, has the built-in ability to do math, just like a calculator. **Arithmetic operators** perform mathematic calculations on numbers, or variables that represent numbers. You already know the most common of these — addition, subtraction, multiplication, and division.

#### Addition

The addition operator, represented by a plus sign (`+`), will add two values and return the sum.

    var x = 2 + 2; // x returns 4

#### Subtraction

The **subtraction** operator, represented by a minus sign (`-`), will subtract two values and return the difference.

```javascript
var x = 10 - 7; // x returns 3
```

#### Multiplication

The **multiplication** operator, represented by an asterisk (`*`), will multiply two values and return the product.

    var x = 4 * 5; // x returns 20

#### Division

The **division** operator, represented by a forward slash (`/`), will divide two values and return the quotient.

    var x = 20 / 2; // x returns 10

#### Modulus

Slightly less familiar is the **modulus** operator, which returns the remainder after division, and is represented by the percentage sign (`%`).

    var x = 10 % 3; // returns 1

`3` goes into `10` three times, with `1` remainder.

#### Increment

A number will be incremented by one with the **increment** operator, represented by a double plus sign (`++`).

    var x = 10;
    x++; // x returns 11

This happens post assignment. It is also possible to write `++x;` which happens prior to assignment. Compare:

    var x = 10;
    var y = x++;
    // y is 10, x is 11

And:

    var x = 10;
    var y = ++x;
    // y is 11, x is 11

#### Decrement

A number will be decremented by one with the **decrement** operator, represented by a double minus sign (`--`).

    var x = 10;
    x--; // x returns 9

As above, it is also possible to write `--x;`.

### Comparison Operators

**Comparison operators** will evaluate the equality or difference of two values and return `true` or `false`. They’re usually used in logical statements.

#### Equal

Two equals signs (`==`) means **equal** in JavaScript. It’s easy to be confused between single, double, and triple equals signs when you’re first learning, but remember that a single equals sign applies a value to a variable, and never evaluates equality.

    var x = 8;
    var y = 8;
    
    x == y; // true

This is a loose type of equality, and will return `true` even if a string is used instead of a number.

    var x = 8;
    var y = "8";
    
    x == y; // true

#### Strict Equal

Three equals signs (`===`) means **strict equal** in JavaScript.

    var x = 8;
    var y = 8;
    
    x === y; // true

This is a more frequently used and more accurate form of determining equality than the regular equal (`==`), since it requires both the type and value to be the same to return `true`.

    var x = 8;
    var y = "8";
    
    x === y; // false

#### Not Equal

An exclamation point followed by an equals sign (`!=`) means **not equal** in JavaScript. This is the exact opposite of `==`, and will only test value, not type.

    var x = 50;
    var y = 50;
    
    x != y; // false

It will treat this string and number as equal.

    var x = 50;
    var y = "50";
    
    x != y; // false

#### Strict Not Equal

An exclamation point followed by two equals signs (`!==`) means **strict not equal** in JavaScript. This is the exact opposite of `===`, and will test both value and type.

    var x = 50;
    var y = 50;
    
    x !== y; // false

It will treat this string and number as unequal.

    var x = 50;
    var y = "50";
    
    x !== y; // true

#### Less Than

Another familiar symbol, **less than** (`<`) will test if the value on the left is less than the value on the right.

    var x = 99;
    var y = 100;
    
    x < y; // true

#### Less Than or Equal To

**Less than or equal to** (`<=`) is the same as above, but equal will also evaluate to `true`.

    var x = 100;
    var y = 100;
    
    x <= y; // true

#### Greater Than

**Greater than** (`>`) will test if the value on the left is greater than the value on the right.

    var x = 99;
    var y = 100;
    
    x > y; // false

#### Greater Than or Equal To

**Greater than or equal to** (`>=`) is the same as above, but equal will also evaluate to `true`.

    var x = 100;
    var y = 100;
    
    x >= y; // true

### Logical Operators

A logical statement will often use the comparison operators we just learned, to determine a `true` or `false` value. There are three additional operators that can be used in these statements to test for `true` or `false`.

It’s important to understand these operators before moving on to conditional statements.

#### And

**And** is represented by two ampersands (`&&`). If both the statements to the left and right of `&&` evaluate to `true`, the whole statement returns `true`.

    var x = 5;

    x > 1 && x < 10; // true

In the above example, `x` is equal to `5`. With my logical statement, I’m testing if `x` is greater than `1` and less than `10`, which it is.

    var x = 5;

    x > 1 && x < 4; // false

The above example returns `false` because even though `x` is greater than `1`, `x` is not less than `4`.

#### Or

**Or** is represented by two pipes (`||`). If either one of the statements to the left and right of the `||` is evaluates to `true`, the statement will return `true`.

    var x = 5;

    x > 1 || x < 4; // true

`x` is not less `4`, but it is greater than `1`, so the statement returns `true`.

#### Not

The last logical operator is **not**, represented by an exclamation point (`!`), which returns `false` if the statement is `true`, and `true` if the statement is `false`. It also returns `false` if a value exists (that does not evaluate to `false`). Take a second to digest that …

    var x = 99;

    !x // false

Since `x` exists and has a value, `!x` will return `false`. We can also test a Boolean value – if the value is `false`, we can test it using the `!` operator, it will return `true`.

    var x = false;

    !x // true

This operator might seem confusing now, but it will make sense as we move into the next section — conditional statements.

### Operator Precedence

When you learned math in school, you may have learned the PEMDAS (_Please Excuse My Dear Aunt Sally_) acronym to learn the Order of Operations. This stands for “Parentheses, Exponents, Multiplication, Division, Addition, Subtraction” – the order in which mathematical operations must be executed.

The same concept applies to JavaScript, except it includes more types of operators. For a full table of of operator precedence, [view the reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence).

Of the operators we learned, here is the correct order of operations, from highest to lowest precedence.

*   Grouping (`()`)
*   Not (`!`)
*   Multiplication (`*`)
*   Division (`/`)
*   Modulus (`%`)
*   Addition (`+`)
*   Subtraction (`-`)
*   Less than (`<`)
*   Less than or equal (`<=`)
*   Greater than (`>`)
*   Greater than or equal (`>=`)
*   Equal (`=`)
*   Not equal (`!=`)
*   Strict equal (`===`)
*   Strict not equal (`!==`)
*   And (`&&`)
*   Or (`||`)
*   Assignment (`=`)

By way of an example, what do you expect the value of `x` to be in the following snippet?

    var x = 15 - 5 * 10;

Well done if you said `-35`. The reason for this result is that the multiplication operator takes precedence over the subtraction operator and the JavaScript engine first evaluates `5 * 10` before subtracting the result from `15`.

To alter operator precedence you can use parentheses.

    var x = (15 - 5) * 10;
    // x is 100

## Conditional Statements

If you’ve ever encountered a block of JavaScript code, you’ve most likely noticed the familiar English words `if` and `else`. These are **conditional statements**, or blocks of code that execute based on whether a condition is `true` or `false`.

All the comparison and logical operators we just learned will come in handy when evaluating these statements.

Conditional statements can be thought of as flow charts that will produce different outcome based on different results.

### If / Else

#### If

An **if statement** will always be written with the keyword `if`, followed by a condition in parentheses (`()`), and the code to be executed in curly braces (`{}`). This would be written as `if () {}`. Since `if` statements usually contain a larger amount of code, they’re written on multiple lines with indentation.

    if () {
    }

In an `if` statement, the condition will only run if the statement in parentheses is `true`. If it is `false`, the entire block of code will be ignored.

    if (condition) {
      // execute code
    }

First, it can be used to test for the existence of a variable.

    var age = 21;

    if (age) {
      console.log("Your age is " + age + ".");
    }

In the above example, an `age` variable exists, therefore the code will print to the console. `if (age)` is shorthand for `if (age === true)`, since the `if` statement evaluates to `true` by default.

We can use the comparison operators we learned earlier to make this condition more powerful. If you’ve ever seen the website for an alcoholic product, they usually have an age limit you must enter to view the site. In America, the age is 21\. They might use an `if` statement to test if the user’s age is greater than or equal to 21.

    var age = 21;

    if (age >= 21) {
      console.log("Congratulations, you can view this site.");
    }

#### Else

If you wanted to display a different message for users who don’t meet the condition, you would use an **else statement**. If the first condition isn’t true, the first code block will be ignored and the `else` code block will be executed.

    if (condition) {
      // execute code
    } else {
      // execute other code
    }

Here is an example with a younger user. Since the user does not meet the condition, the second code block will run.

    var age = 18;

    if (age >= 21) {
      console.log("Congratulations, you can view this site.");
    } else {
      console.log("You must be 21 to view this site.");
    }

#### Else If

If there are more than two options, you can use an **else if statement** to execute code based on multiple conditions.

    var country = "Spain";

    if (country === "England") {
      console.log("Hello");
    } else if (country === "France") {
      console.log("Bonjour");
    } else if (country === "Spain") {
      console.log("Buenos días");
    } else {
      console.log("Please enter your country.");
    }

In the above example, the output will be `"Buenos Días"` since the value of `country` is set to `"Spain"`.

### Switch

There is another type of conditional statement, known as a **switch statement**. It is very similar to an `if` statement, and performs the same function, but is written differently.

A `switch` statement is useful when evaluating many possible outcomes, and is usually preferable to using many `else if` statements.

A switch statement is written as `switch () {}`.

    switch (expression) {
      case x:
        // execute code
        break;
      case y:
        // execute code
        break;
      default:
        // execute code
    }

Within the statement, you’ll see the `case`, `break`, and `default` keywords. We’ll use the same example as we did for `else if` with a switch statement to understand better.

    var country = "Spain";

    switch (country) {
      case "England":
        console.log("Hello");
        break;
      case "France":
        console.log("Bonjour");
        break;
      case "Spain":
        console.log("Buenos días");
        break;
      default:
        console.log("Please enter your country.");
    }

In this example, we’re evaluating the variable for a certain string, and a block of code will execute based on each `case`. The `break` keyword will prevent further code from running once a match is found. If no match is found, the `default` code block will execute, similar to an `else` statement.

## Functions

A JavaScript **function** is a contained block of code. It can perform a task or calculation and accept arguments. One of the main reasons to use a function is to write reusable code that can produce different results each time it is run (depending on the values passed to it).

### Declaration

Before a function can be used, it must be declared (or defined). A function is declared with the `function` keyword, and follows the same rules for naming as variables.

A function is written as `function() {}`. Here is a simple “Hello, World!” in a function.

    function greeting() {
      return "Hello, World!";
    }

### Invocation

In order to invoke (use) the function, type the name followed by parentheses.

    greeting(); // returns "Hello, World!"

### Parameters and Arguments

A function can also accept arguments and perform calculations. An **argument** is a value passed into a function. A **parameter** is a local variable that the function accepts and executes.

> A local variable is a variable that will only work inside a specific code block.

In the example, we’re creating a function called `addTwoNumbers` that, well, adds two numbers together (seriously, good naming is important). We will send the numbers `7` and `3` through as arguments, which will be accepted by the function as the parameters `x` and `y`.

    function addTwoNumbers(x, y) {
      return x + y;
    }
    
    addTwoNumbers(7, 3); // returns 10

Since `7` + `3` = `10`, the function will return `10`. Below, you will see how functions are reusable, as we’ll pass different arguments to the exact same function to produce a different output.

    function addTwoNumbers(x, y) {
      return x + y;
    }
    
    addTwoNumbers(100, 5); // returns 105

There are a couple of other ways of declaring functions in JavaScript. You can read more about those in this article: [Quick Tip: Function Expressions vs Function Declarations](https://www.sitepoint.com/function-expressions-vs-declarations/).



## Conclusion

In this article, we learned three very important fundamental concepts of JavaScript: operators, conditional statements, and functions. Operators are symbols that perform operations on data, and we learned about assignment, arithmetic, comparison, and logical operators. Conditional statements are blocks of code that execute based on a true or false result, and functions are contained blocks of reusable code that perform a task.

With this knowledge, you’re ready to move on to more intermediate concepts of JavaScript. If you have any questions or comments about the material presented, I’d be happy to hear them in the comments below (all the more so if you’re just getting your feet wet with JavaScript).

_This article was peer reviewed by [James Kolce](https://www.sitepoint.com/author/jkolce) and [Tom Greco](https://www.sitepoint.com/author/tgreco/). Thanks to all of SitePoint’s peer reviewers for making SitePoint content the best it can be!_
