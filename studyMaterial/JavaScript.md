
This is the journey of me learning Font-End Developer with Altimetrik Bootcamp


# **JavaScript**


JavaScript is a lightweight, interpreted programming language with object-oriented capabilities that allows you to build interactivity into otherwise static HTML pages.

**Key Points**

* It´s is complementary to and integrated with HTML and Java.
* Desingned for creating network-centric applications.
* It´s an open and cross-platform

<br>

---
<br>

## **Syntaxis and Basic construct**

### **Statements**
Statements are the commands to tell the browser to what action to perform. <br>**Statements are separated by semicolon (;)**


Following table shows the various JavaScript Statements 



| Statment    | Description                                                                                                                                                                                                                       |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **if else**     | The if statement is the fundamental control statement that allows JavaScript to make decisions and execute statements conditionally.                                                                                              |
| **switch case** | A block of statements in which execution of code depends upon different cases. The interpreter checks each case against the value of the expression until a match is found. If nothing matches, a default condition will be used. |
| **while**| The purpose of a while loop is to execute a statement or code block repeatedly as long as expression is true. Once expression becomes false, the loop will be exited.                                                             |
| **do while**    | Block of statements that are executed at least once and continues to be executed while condition is true.                                                                                                                         |
| **for**         | Same as while but initialization, condition and increment/decrement is done in the same line.                                                                                                                                     |
| **for in**      | This loop is used to loop through an object's properties.                                                                                                                                                                         |
|**return**|Used to return a value from a function.|
|**var**|Used to declare a variable.|
|**try**|A block of statements on which error handling is implemented.|
|**catch**|A block of statements that are executed when an error occur.|
|**throw**|Used to throw an error.|
| **continue**    | The continue statement tells the interpreter to immediately start the next iteration of the loop and skip remaining code block.                                                                                                   |
| **function**    | A group of reusable code which can be called anywhere in your programme. The keyword function is used to declare a function.                                                                                                      |
| **break**       | Used to exit a loop early, breaking out of the enclosing curly braces                                                                                                                                                             |

<br>

---
<br>

### **Comments in JavaScript**
<br>

* Any text between a // and the end of a line is treated as a comment and is ignored by JavaScript.
* Any text between the characters /* and */ is treated as a comment. This may span multiple lines.
* JavaScript also recognizes the HTML comment opening sequence <!--. JavaScript treats this as a single-line comment, just as it does the // comment.-->
* The HTML comment closing sequence --> is not recognized by JavaScript so it should be written as //-->.

***Example***

```

          // this is a comment. It is similar to comments in C++

          /*
             * This is a multiline comment in JavaScript
             * It is very similar to comments in C Programming
          */

```

<br>


---

<br>

### **Variables**
<br>

Variables can be referred as named containers for storing information. We can place data into these containers and then refer to the data simply by naming the container.

<br>

### **Rules to declare variable in JavaScript**
<br>

**Before you use a variable in a JavaScript program, you must declare it.**

* In JavaScript variable names are case sensitive i.e. a is different from A.
* Variable name can only be started with a underscore ( _ ) or a letter (from a to z or A to Z), or dollar ( $ ) sign.
* Numbers (0 to 9) can only be used after a letter.
* No other special character is allowed in variable name.


Variables are declared with **var**; as seen previously:

        var money;
        var name, age;
          
**They can be initialized at time of declaration or after:**

            var name = "Ali";
            var money;
            money = 2000.50;
<br>

---
<br>

### **Javascript Data Type**

There are tow kind of data types:

* Primitive Data
* Non Primitive Data

**Primitive types** are the most basic data types available within the Java language. <br>
They are the ones with which we can build abstract data types and data structures.

<br>

The following table describes **Primitive Data Types**
<br>


| Data type    | Description                                                                                                |
| ------------ | ---------------------------------------------------------------------------------------------------------- |
| **String**   | Can contain groups of character as single value. It is represented in double quotes.E.g. var x= “tutorial” |
| **Numbers**  | Contains the numbers with or without decimal. E.g. var x=44, y=44.56;                                      |
| **Booleans** | Contain only two values either true or false. E.g. var x=true, y= false.                                   |
| **Undefined**|Variable with no value is called Undefined. E.g. var x;|
| **Null**|If we assign null to a variable, it becomes empty. E.g. var x=null;|

<br>
<br>

**Non-primitive data** types refer to **objects**. They cannot store the value of a variable directly in memory


The following table describes **Non-Primitive Data Types**



| Data type | Description |
| -------- | -------- |
|**Array**|Can contain groups of values of same type. E.g. var x={1,2,3,55};|
| **Objects**| Objects are stored in property and value pair. E.g. var rectangle = { length: 5, breadth: 3};|

<br>
<br>


---


### **Functions**
<br>

**A group of reusable statements** (Code) that can be **called any where in a program**. In javascript function keyword is used to declare or define a function.

<br>

**Key Points**

* To define a function use the **function** keyword followed by the **name you want to assign**, followed by **parentheses ()**.
* In **parenthesis**, we define **parameters or attributes.**
* The group of reusabe statements (code) is **enclosed in curly braces** **{}**. This code is executed whenever function is called.

***Example***

    function imAnExample (p1, p2) {
       function coding…
    }

<br>


---

<br>

### **Operators**

Operators are used to perform operation on one, two or more operands. Operator is represented by a symbol such as +, =, *, % etc. 

Following are the operators supported by javascript

* Arithmetic Operators
* Comparison Operators
* Logical (or Relational) Operators
* Assignment Operators
* Conditional (or ternary) Operators
* Arithmetic Operators

<br>

**Arithmetic Operators**


| Operator | Description | Example |
| -------- | ----------- | ------- |
|+|Add two operands.|10 + 10 = 20|
|-|Subtract second operand from the first.|10 – 10 = 0|
|*|Multiply two operands.|10 * 30 = 300|
|/|Divide numerator by denominator|10/10 = 1|
|%|It is called modulus operator and gives remainder of the division.|10 % 10 = 0|
|++|Increment operator, increases integer value by one|10 ++ = 11|
|--|Decrement operator, decreases integer value by one|10 -- = 9|

<br>

**Comparison Operators**


| Operator | Description | Example |
| -------- | -------- | -------- |
|==|Checks if values of two operands are equal or not, If yes then condition becomes true.|10 == 10 will give true|
|!=|**Not Equal to operator:** Checks if the value of two operands is equal or not, if values are not equal then condition becomes true|10 !=10 will give false|
|>|**Greater Than operator:** Checks if the value of left operand is greater than the value of right operand, if yes then condition becomes true.|20 > 10 will give true|
|<|**Less than operator:** Checks if the value of left operand is less than the value of right operand, if yes then condition becomes true.|10 < 20 will give true|
|>=|**Greater than or equal to operator:** Checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true.|10 >=20 will give false|
|<=|**Less than or equal to operator:** Checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true.| 10 <=20 will give true.|

<br>

**Logical Operators**



| Operator | Description | Example |
| -------- | ----------- | ------- |
|&&|**Logical AND** operator returns true if both operands are non zero.|10 && 10 will give true.|
|![](https://i.imgur.com/1ZDAl3R.png)|**Logical OR** operator returns true If any of the operand is non zero|10![](https://i.imgur.com/P3Ykuud.png)0 will give true.|
| !|**Logical NOT** operator complements the logical state of its operand.|! (10 && 10) will give false.|

<br>

**Assignment Operators**


| Operator | Description | Example |
| -------- | ----------- | ------- |
|=|**Simple Assignment operator:** Assigns values from right side operands to left side operand.|C = A + B will assign value of A + B into C|
|+=|**Add AND assignment operator:** It adds right operand to the left operand and assign the result to left operand|C += A is equivalent to C = C + A|
|-=|**Subtract AND assignment operator:** It subtracts right operand from the left operand and assign the result to left operand|C -= A is equivalent to C = C - A|
|*=|**Multiply AND assignment operator:** It multiplies right operand with the left operand and assign the result to left operand|C *= A is equivalent to C = C * A|
|/=|**Divide AND assignment operator:** It divides left operand with the right operand and assign the result to left operand|C /= A is equivalent to C = C / A|
|%=|**Modulus AND assignment operator:** Modulus AND assignment operator, It takes modulus using two operands and assign the result to left operand|C %= A is equivalent to C = C % A|

<br>
<br>

**Conditional Operator**

It is also called ternary operator, since it has three operands.

| Operator | Description | Example |
| -------- | ----------- | ------- |
|?|Conditional Expression|If Condition is true? Then value X : Otherwise value Y|

<br>


---

<br>

### **Control Structure**

Control structure actually controls the flow of execution of a program. Following are the several control structure supported:

* if...else
* switch case
* do while loop
* while loop
* for loop

<br>

**If … else**

The if statement is the fundamental control statement that **allows** JavaScript **to make decisions and execute statements conditionally**.

***Example***

        var age = 20;
          if( age > 18 ){
             document.write("<b>Qualifies for driving</b>");
          }

<br>

**Switch case**

Gives an expression to evaluate, and several different statements to execute based on the value of the expression. 
<br>The interpreter **checks each case against the value of the expression until a match is found**. If nothing matches, a default condition will be used.

***Example***

          var grade='A';
          document.write("Entering switch block");
          switch (grade) {
             case 'A': document.write("Good job");
                break;
             case 'B': document.write("Pretty good");
                break;
             case 'C': document.write("Passed");
                break;
             case 'D': document.write("Not so good");
                break;
             case 'F': document.write("Failed");
                break;
             default:  document.write("Unknown grade")
          }
          document.write("Exiting switch block");

<br>

**Do while Loop**

The do...while loop is **similar to the while loop except that the condition check happens at the end of the loop**. <br>This means that the **loop will always be executed** at **least once**, even if the condition is false.

***Example***

          var count = 0;
          document.write("Starting Loop" + "<br/>");
          do{
             document.write("Current Count : " + count + "<br/>");
             count++;
          }while (count < 0);
          document.write("Loop stopped!");

This will produce following result:

    Starting Loop
    Current Count : 0
    Loop stopped!


<br>

**While Loop**

The purpose of a while loop is to **execute a statement or code block repeatedly as long as expression is true**. <br>Once expression **becomes false**, the **loop will be exited**.

***Example***

          var count = 0;
          document.write("Starting Loop" + "<br/>");
          while (count < 10){
             document.write("Current Count : " + count + "<br/>");
             count++;
          }
          document.write("Loop stopped!");

This will produce following result: 

    Starting Loop
    Current Count : 0
    Current Count : 1
    Current Count : 2
    Current Count : 3
    Current Count : 4
    Current Count : 5
    Current Count : 6
    Current Count : 7
    Current Count : 8
    Current Count : 9
    Loop stopped!


<br>

**For Loop**

The for loop is the most compact form of looping and includes the following three important parts:

* The **loop initialization** where we initialize our counter to a starting value. The initialization statement is executed before the loop begins.
* The **test statement** which will test if the given condition is true or not. If condition is true then code given inside the loop will be executed otherwise loop will come out.
* The **iteration statement** where you can increase or decrease your counter.

***Example***

          var count;
          document.write("Starting Loop" + "<br/>");
          for(count = 0; count < 10; count++){
             document.write("Current Count : " + count );
             document.write("<br/>");
          }
          document.write("Loop stopped!");

This will produce following result which is similar to while loop:

    Starting Loop
    Current Count : 0
    Current Count : 1
    Current Count : 2
    Current Count : 3
    Current Count : 4
    Current Count : 5
    Current Count : 6
    Current Count : 7
    Current Count : 8
    Current Count : 9
    Loop stopped! 

<br>


---
<br>

## **Bibliography**

 https://www.freecodecamp.org/
