# META Programming with Java labs
# Lab Instructions: Object Oriented Programming
 
## Task 1: Code a Person class

Code a Person class, with three parameters in the constructor: name, age, and energy.

Set the default parameters in the Person class as follows:

```
name = "Tom"

age = 20

energy = 100
```

Code two methods in the `Person` class. Name those methods `sleep()` and `doSomethingFun()`.

The `sleep()` method should take the existing energy level and increase it by 10.

The doSomethingFun() method should take the existing energy level and decrease it by 10.
<br><br>

## Task 2: Code a Worker class

Code a sub-class, inheriting from the `Person` class, and name it `Worker`.

The `Worker` class has two additional parameters in the constructor: 
- xp (for "experience points")
- hourlyWage.

These properties are set to the following default values:
```
xp = 0

hourlyWage = 10
```
The `Worker` class has all the paramerters and methods of its super-class.

Additionally, it has the `goToWork()` method, which, whenever it's run, increases the value of the `xp` property by 10.
<br><br>

## Task 3: Code a intern object

Inside the intern function instantiate the `Worker` class to code a new intern object.

The intern should have the following characteristics:
```
name: Bob

age: 21

energy: 110

xp: 0

hourlyWage: 10
```

Run the `goToWork()` method on the intern object. Then `return` the intern object.

<br><br>


## Task 4: Code a manager object

Inside the manager function instantiate the `Worker` class to code a new `manager` object.

The manager object should have the following characteristics:
```
name: Alice

age: 30

energy: 120

xp: 100

hourlyWage: 30
```

Run the `doSomethingFun()` method on the manager object. Then `return` the manager object.

<br><br>


# Lab Instruction: Iterate Over an Array

In this exercise, you'll use the for....of loop to iterate over an array and to iterate over an object's own properties.  
<br><br>
**Step 1.** You are given an array of dairy products:  

    
    var dairy = ['cheese', 'sour cream', 'milk', 'yogurt', 'ice cream', 'milkshake']
    


Create a function called `logDairy`. Within it, console log each of the items in the dairy array, using the for...of loop.   
The expected output should be:

```
cheese
sour cream
milk
yogurt
ice cream
milkshake
```

<br>
<b>Step 2.</b> You are given the following starter code:  

```
const animal = {

canJump: true

};

const bird = Object.create(animal);

bird.canFly = true;

bird.hasFeathers = true;
```

Create a function called `birdCan`, within it, loop over the bird object's properties and console log each one, using the for...of loop.
Remember, you need to console log both the key and the value of each of the bird object's properties.

<br>
<b>Step 3.</b> 
    Using the same starter code as in task 2, create a function called `animalCan` and within it, loop over all the properties in both the bird object and its prototype - the animal object - using the for...in loop. 
    
<br>
<br>

# Lab Instructions: Building a Functional Program

In this exercise you'll get hands-on practice with functional programming concepts. <br> <br> 

## Task 1: Build a function-based console log message generator
In this exercise, your task is to code a function named `consoleStyler`, which accepts four parameters:
- `color`
- `background`
- `fontSize`
- `txt`

Inside the body of the consoleStyler() function declaration, you need to do the following:

1. Create a new variable named message, and assign the following to it on the very first line inside the consoleStyler() function body.: 
    ```
    "%c" + txt;
    ```

2. Create a style variable and assign the following to it on the next line: 
    ```
    `color: ${color};`
    ```

3. Next, update the style variable (using the += operator) with the following code: 
    ```
    `background: ${background};`
    ```

4. Then, update the style variable (again, using the += operator) with the following code: 
    ```
    `font-size: ${fontSize};`
    ```

5. Finally, console log the message and style variables inside the `consoleStyler` function declaration.

Hint: Be sure to use backticks (``) when updating your variable styles and not single ('') or double ("") quotes.

<br>

## Task 2: Build another console log message generator. 

Your task is to code another function, and name it `celebrateStyler()`. The function accepts a single parameter, reason, which should be of string data type.

Inside the function declaration's body, code the following: 

1. A new variable, named fontStyle, assigning it this code:
    ```
    "color: tomato; font-size: 50px";
    ```

2. On the next line, an if statement, verifying that `reason == "birthday"`. 

3. Inside the body of the if block, code the following: 
    ```
    console.log(`%cHappy birthday`, fontStyle);
    ```

4. On the next line, add an else if, and inside the parentheses, check that 
    ```
    reason == "champions"
    ```

5. Inside the else if block, add this code: 
    ```
    console.log(`%cCongrats on the title!`, fontStyle);
    ```

6. Add an else block, with the following code inside of it: 
    ```
    console.log(message, style);
    ```

<br>

## Task 3: Run both the consoleStyler and the celebrateStyler functions

1. Invoke the consoleStyler() function, with the following arguments:

    - `'#1d5c63'`

    - `'#ede6db'`

    - `'40px'`

    - `'Congrats!'`

2. Next, invoke the celebrateStyler() function, with the following argument:

    - `'birthday'`


## Task 4: Insert a congratulatory and custom message

1. Code another function, named `styleAndCelebrate()`.   
The function declaration's body should consist of two function invocations:
    ```
    consoleStyler(color, background, fontSize, txt);  
    celebrateStyler(reason);
    ```


2. Next, invoke the new function, using the following arguments:

    - `'ef7c8e'`
    - `'fae8e0'`
    - `'30px'`
    - `'You made it!'`
    - `'champions'`

<br>

# Lab Instructions: Jest unit testing

## Task 1: Code the timesTwo function

Open the timesTwo.js file and add a function named `timesTwo`. The function should take number as input and return the value 2 multiplied by the number.
Export the timesTwo function as a module.
<br><br>

## Task 2: Write the first test
Code a test call with the following arguments:
1. The description that reads: "returns the number times 2".
2. The second argument should expect the call to the timesTwo function, when passed the number 10, to be 20.
   <br><br>

## Task 3: Run the first test
With the terminal pointed at the `jest-testing` directory, run the test script using npm.