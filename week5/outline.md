# Intro to Web Dev

## Week 5 Outline

### As you come in:

* Navigate to [nerdyperson.com](http://www.nerdyperson.com) (This webpage)
* Complete the warmup exercise:

Here's a new HTML element:

```
<button> </button>
```

Figure out how to render this into the body of an HTML document.
Experiment with the following:
* Nest a text node inside the button (add text to the button)
* Can you select and style the element using CSS?
* Can you make this button into a link, wrapping it with an anchor tag?
* Read the [docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) and experiment with other attributes!

### Motivation/Project
Using JavaScript, we're eventually going to take our cloud project from two week and rework it so that instead of just running when the user loads the page, we can create a button that will allow the user to turn on the animation.

🙃 Reminder! Here's the keyboard shortcut for opening the Chrome Developer Tools / Console: Control+Shift+J

## JavaScript functions

JavaScript functions are used to wrap a code block so that you can control when that code gets executed.  Here's the general format for a **function definition**.  Note the ```//``` symbol "comments out" the line, so it won't get executed. In this case, you would replace the line starting with ```//``` with your actual code.
```
function nameOfFunction(){
  // your code goes here
}
```
To use your function, you need to invoke it, using the name of the function plus parentheses like so:
```
nameOfFunction();
```

Here are some examples of simple functions.  Can you reason about what they do?

```
function doSomething(name){
    return 'Welcome to ' + name + ' Berkeley Public Library!!!';
}

function addNums(num1, num2){
  var someSum = num1 + num2;
  return someSum;
}

function changeColor(){
  body.style.backgroundColor = 'red';
}

```
Some functions can explicitly return a value, like the first and second functions in the example above.  Other functions might make changes to the state of our webpage, for example, a function can change DOM elements, and not explicitly return anything (in that case, the function will return ```undefined```).

Your function can take an input.  If you build your function to take in input, you would declare that in the function definition.  In the examples above, ```addNums()``` and ```doSomething()``` both take inputs.  How many inputs do each of those functions take?

Here are the invocations for all of the functions written above.   These lines "turn on" and run the functions declared above. We can invoke a function as many times as we'd like.

```
doSomething('Bob');
addNums(1,2);
changeColor();

// We can keep invoking these as we'd like:

doSomething('Mary');
doSomething('Beth');
addNums(100000,999);
changeColor();
changeColor();
changeColor();

```
Question: After we've run changeColor() once on a page, what will happen if we try to run it again?


### console.log() revisited
Remember those parentheses at the end of ```console.log()```?  ```console.log()``` is a function also! It's a built in function in JavaScript.  As you remember, ```console.log``` takes in an input, and spits that input out into the console that we can see in the Chrome Developer tools. You can pass expressions to console.log() that will get evaluated before they hit the console, including functions!

```
// review from last week:

console.log('Berkeley');
console.log(100);

console.log('Reading' + ' is cool!!');
console.log(100 + 1);

// now, more exciting:

console.log(addNums(1,2));
console.log(addNums(100,1));
console.log(doSomething('Richard'));

```
```console.log()``` is really useful to let us debug functions and see if we're getting the expected output/return value!




### onclick events

During the warmup exercise, we experimented with the ```<button>``` HTML element.  Now let's use its ```onclick``` attribute to wire buttons to functions.

We can pass function invocations to the ```onclick``` attribute like so:

```
<button onclick="myFunction()">Run my function!</button>
```

### Exercise - wiring functions and buttons
In our example, we have some functions in the ```<script>``` section of the page.  Can you figure out how to add them to the buttons via the ```onclick``` attribute?

Before you begin, notice the functions in this HTML document.  Do any of these functions take input or have output?  What type of function are these?

```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <style>
        #sun{
          width: 100px;
          height: 100px;
          background: yellow;
          border-radius: 100%;
          animation-duration: 5s;
          position: absolute;
          border: 3px dotted orange;
          bottom: 0%;
          left: 50%;
          animation-iteration-count: infinite;
        }

        @keyframes raiseTheSun{
          0%{
            bottom: 0%;
          }

          100%{
            bottom: 100%;
          }
        }
        </style>
    </head>
<body>
  <div id="sun"></div>

  <button>Sunrise!</button>
  <button>Turn Off the Lights!</button>
  <button>Build A Fence!</button>

  <script>
  function sunRise(){
    const sun = document.querySelector('#sun');
    sun.style.animationName = 'raiseTheSun';
  }

  function turnOffLights(){
    document.body.style.background = '#000';
  }

  function buildAFence(){
    document.body.style.border = '10px dotted tan';
  }

  </script>
</body>
</html>

```

Stretch goals:
* Change the actions that the buttons trigger
* Add another button and make it perform another action (write another function!)
* Add buttons that reverse the current actions


### End of Class
* Submit your work for class credit.  On your desktop, create a folder with your name.  Put your work into that folder.  Drag the folder into the shared folder [here](https://drive.google.com/drive/folders/15pl4yzGx6OhXQKHbW8g1cKAkvKkaJenn?usp=sharing).


### Further Exploration
* [FreeCodeCamp exercises](https://www.freecodecamp.org): Keep going!
* Check out other computer-related events at the (Library)[https://www.berkeleypubliclibrary.org/events/computers]!
* [W3Schools Intro to JavaScript](https://www.w3schools.com/js/js_intro.asp)
* Advanced: [You Don't Know JavaScript](https://github.com/getify/You-Dont-Know-JS)
