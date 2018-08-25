# Intro to Web Dev

## Week 4 Outline

### As you come in:

* Navigate to [nerdyperson.com](http://www.nerdyperson.com) (This webpage)
* Complete the warmup exercise:

Your friend needs some help building their webpage.  They have the basic structure set up, but they need your help wiring IDs and classes to their appropriate elements on the page. 

```
```

### Chrome Developer Tools
One big themes of this course is making the transition from a person who passively consumes web content to someone who produces their own web pages. You already used part of Chrome Developer tools on the first day to inspect the code generating your favorite website.  Now we're going to dive deeper into these tools that will help you inspect and build websites.  Chrome Developer tools play a big role in our exploration of JavaScript.

## Motivation
We can use JavaScript to take in input from a user and make changes to the state of our page. Let's take the example of the cloud from last week and rework it so that, instead of just running when the user loads the page, we can create a button that will allow the user to turn on and off the animation.

## Open Dev Tools
In Google chrome, {PC Shortcut}

### JavaScript
JavaScript is a programming language that, along with CSS and HTML, allows us to build interactive web pages.

Here are the main categories or types of things that we'll be interacting with in JavaScript.

Picture JavaScript as a vast ocean.  There are a number of different fish swimming around in this ocean.  In reality, this is a bit more complicated, but for our purposes, these are the fish in our sea:
(Note, don't get hung up on the specifics or syntax of functions yet in case you are unfamiliar with them - we'll explore functions in more detail separately.)

* Strings - strings are text or characters, including numbers, and spaces, wrapped with single or double quotation marks
* Numbers
```
4
-50
100
5.522
```
* Boolean - true or false
```
true
false
```
* Document Objects - All of the html elements we've already worked with.  Essentially any piece of a webpage that we want to target for some sort of interaction or modification.
```
<h1>My Header</h1>
<div id="redBox"></div>
<a href="#">Link to Nowhere</a>
```
* Function - a way to wrap some code in a reusable chunk
```
function changeBodyColor(){
  document.body.style.backgroundColor = 'red';
}

function addNums(num1, num2){
  return num1 + num2;
}
```

The console is a place for us to input and interact with the page.

Let's log some stuff to the console:
What happens when you type the following lines into the console and hit the return key?
```
1 + 100;
"Berkeley";
"Berkeley" + 100;
1 === 1;
1 === 2;
"Berkeley" === "El Cerrito";
5 > 3;
10000 < 1;
true === false;
true === true;
```
>>> Exercise: from the list above, which ***types*** are we using in the above examples?

Each line gets evaluated and returns some value.
Congratulations! You're already writing JavaScript.

## Console.log()
In order to keep working with JavaScript in our actual HTML document, we're going to use a JavaScript built in function called console.log(). We use console.log() when we want to send stuff to be evaluated from our HTML.

Console.log is a built in function in JavaScript.  For our purposes, it lets us send things to the console in Chrome Developer tools.  It's mostly used for debugging purposes.

### Script Tag
Now we're going to add another section to our HTML document, the script section.  Since we want the JavaScript most likely to run and change pieces of the HTML we've written, it's a good idea to put the ```<script>``` section at the bottom of and inside the ```<body>``` tag.

>>> Exercise: Write some expressions and send them to the console using console.console.log();

```
console.log(1 + 2);
console.log("hi mom!");
```

### Architecting the problem
Putting aside the computer for a moment, let's think through the logic of adding a button.  Review from last class how the cloud moved across the screen.  How can we enable or disable that from happening?  How could we animate this "the hard way"?


### Modifying styling with JavaScript

Let's start with this template.  Before you render it in the browser, check to see if you can reason about what it does:

```
<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <style>
      .redBox{
        width: 100px;
        height: 100px;
        background-color: red;
        position: absolute;
        top: 0px;
        left: 0px;
      }
    </style>
  </head>
  <body>
    <div class="redBox"></div>
  </body>
</html>
```

Now let's change that redbox using JavaScript.  Add a ```<script></script>``` section nested inside and at the bottom of the ```<body>``` element.

Here's some JavaScript:  Can you reason about what it's doing?

>>> Warning: Note in JavaScript, the style names aren't written with dashes, but instead using the camel case convetion, which means three things:
* start with a lower case letter
* no spaces
* each word after the first word has an uppercase letter


```
var redBox = document.querySelector('.redBox');
redBox.style.backgroundColor = 'blue';
```

The first line declares a new variable, or var, in memory, and then assigns using the ```=``` sign it to the expression document.querySelector('.redBox').


### Animate the redBox.
Keep writing new scripts to update the position of the redbox one pixel at a time.

```
var redBox = document.querySelector('.redBox');
redBox.style.left = '1px';
```


### onclick events

Here's another html element, the button.  Add it to your body:
```
<button></button>
```
What does it render as when you refresh the page?

The button element takes an attribute, ```onclick``` which we can pass data to.
Try this:

Warning: the formatting must be exactly the same!
```
<button onclick="console.log('clicked the button')"></button>
```



### Exercise - wiring functions and buttons
In our example, we have some functions

## querySelector
So far we've been interacting with numbers, booleans and strings.   Now let's access some part of the page.
QuerySelector will return the first instance of the input that matches our request.
document.querySelector

### End of Class
* Submit your work for class credit.  On your desktop, create a folder with your name.  Put your work into that folder.  Drag the folder into the shared folder [here](https://drive.google.com/drive/folders/1xwPCotd3c9eIDqwDBhg_UEZ_QJETePuR?usp=sharing). 

### Further Exploration
 * [FreeCodeCamp exercises](https://www.freecodecamp.org): “Front End Development Certifications” > “HTML5 and CSS” – complete all of the exercises there (through “Use RGB to Mix Colors”)
* Read more about CSS Animations [here](https://www.w3schools.com/css/css3_animations.asp)