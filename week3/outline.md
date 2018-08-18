# Intro to Web Dev

## Week 3 Outline

### As you come in:

* Navigate to [nerdyperson.com](http://www.nerdyperson.com) (This webpage)
* Complete the warmup exercise:

* Open the Sublime application on your computer (if you can't find Sublime, click the Windows icon in the lower left hand corner of the screen. In the text box that appears, type ```Sublime```. You should see Sublime appear in the applications list).
* Paste in our basic HTML starter document:

```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <style></style>
    </head>
<body>
</body>
</html>
```
* Save as an HTML document on the Desktop. Remember the file format:
```xxxx.html```
* Simultaneously open your newly saved webpage in Chrome.

😎 ProTip You can quickly generate an empty HTML template in Sublime. After you have already saved your file as a *.html file somewhere on your local computer, type <h. You will see a menu appear. If you press the tab key, the HTML template will autocomplete.

* Now, create three ```<div>``` elements in the ```<body>``` section of your HTML document.  Don't forget to write your code **between** the opening ```<body>``` tag and the closing ```</body>``` tag.
* Style the div elements accordingly:

```
The first div should be 50px high by 50px wide and have a green background color.

The second div should be 100px high by 150px wide and have a blue background color.

The third div should be 200px high by 250px wide and have a yellow background color.

```
♻ **Review:** How can you apply different styles to different divs?  Remember use **class selectors**.  Here's an example of a class selector if you forgot how to do that:

```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <style>

          .yellowSun{
            background: yellow;
            border: 3px solid orange;
            width: 100px;
            height: 100px;
            border-radius: 100%;
            margin: 0 auto;
          }

        </style>
    </head>
<body>

    <div class="yellowSun"></div>

</body>
</html>

```

💃 If you finish early, add some margins to your divs to spread them out!

## Making our website more dynamic: CSS Animations and Pseudo Selectors

### Pseudo Classes

You can rerender your style completely when a mouse hover event happens using a CSS Pseudo Class.

In this example, we declare a style for an ```h2``` element normally, and then further down in the CSS redeclare the style for a different state (in this case a hover event or the hover pseudo class).

```
h2{
    background-color: yellow;
}

h2:hover{
    background-color: red;
}
```
Here's a translation of the above CSS into English: "Normally, make h2 elements have a yellow background color. But, when someone hovers over h2 elements with their mouse, change the background color to red."

The pseudo class declaration replaces style declarations from the previous declaration.  We can selectively alter properties, while leaving others in tact.  For example, maybe we always want to keep our h2's font size 72px, with 100% width, and text aligned center, but want to change the background color on a hover event:

```
h2{
    font-size: 72px;
    width: 100%;
    text-align: center;
    background-color: yellow;
}

h2:hover{
    background-color: red;
}
```
We reference only the properties we want to update or change. Everything else stays the same!

You can totally transform a previously declared style using a pseudo selector. Let's experiment with pseudoselectors on the divs you created for the warmup exercise!  Try the following:

* On a hover event, change the size of one of your divs.
* On a hover event, change the color of one of your divs.
* On a hover event, change the border-radius on one of your divs.

### CSS animations

CSS animations let us create some really impressive effects using only CSS (no Flash or JavaScript!) This like a more complicated and powerful version of the CSS psuedo classes. First of all, we can use the CSS ```transition``` property to **ease** the transition between states.  In this example, I created a class style called ```myRedBox```.  On a hover event, ```myRedBox``` turns into a smaller circle with a green background.

```
.myRedBox{
    width: 100px;
    height: 100px;
    background: red;
    margin: 15px;
}

.myRedBox:hover{
    border-radius: 100%;
    width: 50px;
    height: 50px;
    background: green;
}

```

The current transition is jarring.  But if I add the ```transition``` property to the original style, I can improve it:

```
.myRedBox{
    transition: ease 1s;
    width: 100px;
    height: 100px;
    background: red;
    margin: 15px;
}

.myRedBox:hover{
    border-radius: 100%;
    width: 50px;
    height: 50px;
    background: green;
}

```

```1s``` stands for "1 second" similar to the px declarations you've already seen.

Experiment with different times and updates using ```transition```!

### @keyframes

The ```@keyframes``` CSS declaration lets us literally create an animation frame by frame.  Each frame is different CSS style.

Let's take one of our example divs from earlier:

```
.redBox{
    width: 100px;
    height: 100px;
    background: red;
}

```
If we want to animate the ```redBox``` we can declare an animation in our CSS file, and then add that animation to the ```redBox```. We use a new declaration called **keyframes** to label our animation:

Inside the ```@keyframes``` declaration, we specify how we want our CSS to look at different moments in time.  Don't forget to name your animation!

```
@keyframes myBoxAnimation{
    }
```

Keyframes let us build different CSS styles at different moments in time. We can start at 0% and declare different styles all the way through 100%:

For example, if we want our box to transition from red to blue to green and back to red, we can write something like this:

```
    @keyframes myBoxAnimation{

     10%{
         background: blue;
         }

     50%{
         background: green;
        }

     100%{
         background: red;
         }
    }

```

♻ **Review:** Do you remember the concept of HTML **nesting**?  CSS keyframes literally nests multiple CSS styles into one segment of CSS.

The percentage refers to the amount of the animation that has completed.  You could theoretically write a new CSS style for every integer between 1 and 100 in this case.

Now all we have to do is add this keyframe property to our ```div```. 

```
.redBox{
    width: 100px;
    height: 100px;
    background: red;
    animation-name: myBoxAnimation;
    animation-duration: 5s;
    animation-iteration-count: 2;
}

```

We also need to add additional properties telling how long to run the animation, and whether to repeat it.


Experiment with other animation style declarations and properties:
```
    animation-name: example;
    animation-duration: 5s;
    animation-delay: -1s;
    animation-iteration-count: infinite;
```

* Read more about CSS Animations [here](https://www.w3schools.com/css/css3_animations.asp)