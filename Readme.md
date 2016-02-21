
#Conditional Statements

A conditional statement is a set of commands that executes based on a set of conditions. We use conditionals in our every day life: "If I don't have time to make an espresso in the microkitchen (conditional), then I'll be grouchy for the entire morning. (code)"

JavaScript has three types of conditional statements:

* **if** executes a block of code if a condition evaluates to true
* **else** executes a block of code if that condition evaluates to false
* **else if** allows for an additional condition to be evaluated

## The if statement

With the if statement, a block of code will only run if the condition is true.

```
if (condition){
  block_1;
}
```
Notice the JavaScript syntax for conditional statements:
+ conditions are in parenthesis,
+ blocks are in curly brackets {}
+ expressions end with ';' semicolons.

Also note that each block is indented. JavaScript doesn't need indentation to work, but indentation improves readability. It's also a good habit to get into now, because many languages like Python are particular about how blocks of code are indented. Do not use tab to indent, instead use 4 spaces. The tab key can be interpreted differently depending on which editor you are using.

An example is shown below. Everyone in the Simpson household is eating healthy and will get a clementine as a snack. The exception is if Homer is in the kitchen.
```
var snack = "clementine";
var name = "Lisa";
if (name == "Homer"){
  snack = "pink donut";
}
```
In the above code, the snack variable still holds the value "clementine" because the condition that name was equal to Homer was not true. Therefore, the block inside the curly brackets is not executed and the snack variable does not get reassigned.

## The if/else statement
The if/else statement is constructed in a similar way to the if statement, except that there is a new block that is automatically executed when the condition is false.
```
if (condition){
    block_1;
} else {
    block_2;
}
```

As an example, let's think about how Bart avoids Nelson but otherwise doesn't care too much about Springfield's other residents.
```
if (student == "Nelson") {
    action = "hide";
} else {
    action = "skate";
}
```

If Bart sees Millhouse, the condition is false, so the first block is skipped. The else statement is executed and Bart skates on.

## The else if addition
If/else statements can be made more complex and more specific by adding an additional conditional statement with `else if`. You can chain multiple `else if` statements together if needed. Your interpreter will check the conditions from top to bottom. As soon as one condition is true, it will execute that block and then skip checking any subsequent conditions.

```
if (condition){
    block_1;
} else if {
    block_2;
} else {
    block_3;
}
```
For example, if it's 11 am (hours=11), the code below tells us that Homer is at his job at the power plant. Each condition is checked from top to bottom until one evaluates to true. As soon as that happens, the block under that condition is executed and the rest of the code is ignored.

```
if (hours>=19) {
    location = "couch";
} else if (hours>=17) {
   location = "Moe's Tavern"
} else if (hours>=9){
    location= "Springfield Nuclear Power Plant"
} else {
   location = "bedroom"
}

```

## Comparison Operators
You’ll notice we’ve been using some new operators in our conditional statements, like '==' and '>='. These are our **comparison operators** - they express conditions like equality and inequality. Comparison operators evaluate to either True or False.

Note that the double '==' is used for comparison. The single '=' is for variable assignment. You (and your future students) will likely make this mistake a few times before getting the hang of it, so it's always a great thing to anticipate when debugging code.

Below is a list of all JavaScript comparison operators and what they do

<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-2.5-conditional-statements/master/js-boolean-operator-table.png">

Conditional statements can have even more complexity if logical operators are included. These let us combine conditions. 

Here is a list of all the Logical Operators and what they do:

<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-2.5-conditional-statements/master/js-logical-operators.png">
