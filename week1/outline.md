# Intro to Web Dev

Welcome to Class!

## Week 1 Outline

### As you come in:
* 🤓 Fill out the [survey](https://goo.gl/forms/fF8ZhRA2XzmCBb9Y2)
* Sign up at [FreeCodeCamp](http://freecodecamp.org)

### Class guidelines
* Everyone is welcome!
* If you miss one or more classes, you can follow along with [FreeCodeCamp](http://freecodecamp.org) and always feel free to sit in on as many classes as you can make.  
* Class is 5 weeks long.  
* Helpful previous knowledge: high school algebra, basic computer skills like navigating webpages
* Thursdays at 10 AM is a [beginner computer class](https://www.berkeleypubliclibrary.org/events/beginner-computer-class-central-ec-0)  
* Attend all five sessions, submit classwork to earn certificate from the library.

### Class goals
* Transition from web consumer to producer/maker/creator
* Build some fun projects: personal webpage, interactive game
* Build foundation so you can keep learning on your own

### Changing perspective from web content consumer to producer
* "Peek behind the curtain" with Chrome developer tools.  Right click: "View Page Source"
* Set up your first html file.  In Notepad, select File > Save As.  Save your file as anything.html 
* Notice, this file isn't a text file anymore! Now it's a webpage file (HTML file)

### HTML Tags
* HTML tags are the building blocks of webpages.  Most tags have an opening and closing tag that you can put stuff between (**nesting**).

This is an opening and closing header tag:
```
<h1> </h1>
```

We can put text between the tags to make a header for our webpage:  
```
<h1> Welcome to my Site </h1>
```

Experiment with some other tags: What do they do?
```
<h1> </h1>
<h2> </h2>
<h3> </h3>
<strong> </strong>
<em> </em>
<p> </p>
```

Some tags only have one component. They open and close themselves at the same time. What do these do?
```
<br />
<hr />
```

### Adding attributes to tags
You can add properties and data called **attributes** to further customize some tags.  Attributes have keys and values.  The key is the name of the attribute, and the value is the data connected to that attribute. Here's a tag to add an image to your webpage:
```
<img> </img>
```

We need to pass an image source (src) to the tag so it can render an actual picture:

```
<img src="mypicture.png"> </img>
```

If you find an image you like, right click and select "Copy image address".  This will copy the source/location of your image for you.

⚠️ 🚨 **Be careful with formatting!  Watch for opening and closing carets and quotation marks!**

Here's how to create a link using the **anchor** tag and the **href** attribute.

```
<a href="http://www.google.com">Link to Google</a>
```

### Nesting HTML Tags
You've already nested text nodes inside of HTML tags.  Now let's try nesting some HTML tags inside of other tags!

These tags in combination make make an unordered list.  Notice how the ```<li>``` tags are ***nested*** inside the outside ```<ul>``` tags:
```
<ul>
    <li>Apples</li>
    <li>Quinoa</li>
    <li>Spaghetti</li>
<ul>
```

Here's an ordered list:
```
<ol>
    <li>preheat oven</li>
    <li>mix ingredients</li>
    <li>bake cake</li>
</ol>
```

### HTML Document
Here's your canvas for doing further work.  We're going to build most of the webpage inside of the ```<body>``` tags:
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

Move your work so far in between the opening and closing ```<body>``` tags.  Don't forget to give your webpage a title in the ```<title>``` section!  (You'll see that title render in the top of your browser tab).

### Styling with CSS
We might want to further customize our HTML tags.  We can do that in the ```<style>``` section of our document:

Here's how we can change the properties of all the paragraph, ```<p>``` tags on our webpage.  This is called a ***CSS selector*** because it **selects** a part of the page we want to target for styling.

```
p{

}
```

Now we can add some properties:
```
p{
    color: green;
    font-family: sans-serif;
}
```

⚠️ 🚨 **Be careful with formatting!  Watch for opening and closing brackets and make sure every line ends with a semicolon!**

Experiment with more properties on your own:

```
p{
    color: green;
    font-family: sans-serif;
}
```

Try targeting another tag like a header:
```
h1{
    background-color: blue;
    color: white;
}
```

What happens if you have multiple ```<p>``` tags on a page?  How do the tags get affected by your styles?

Experiment with more properties:
```
padding: 10px;
margin: 50px;
border: 3px solid black;
border-radius: 80%;
```

### Styling with classes

Sometimes we don't want to target all of our tags of the same time for styling.  We can use a ***class*** to target specific pieces of the page.  
We can add a class attribute to any HTML tag:

Here's our example webpage.  
```
<p>My first paragraph!</p>
<p>My second paragraph!</p>
<p>My third paragraph!</p>

```

If I want to make the ONLY the second paragraph background red with white font, I could write a CSS class selector like this.  I have to give my class selector a name.  In this case, I called it "myStyle".  You can name your classes anything you want as long as you don't use any spaces.  

```
.myStyle{
    background: red;
    color: white;
}
```

⚠️ 🚨 **Be careful with formatting! Classes start with a period! Your style name cannot have any spaces in it!**

Now I have to apply my style class to the second paragraph.  I use the class attribute to lay the style into the page:

```
<p>My first paragraph!</p>
<p class="myStyle">My second paragraph!</p>
<p>My third paragraph!</p>

```

### Using divs

The ```<div>``` is a powerful HTML tag.  We can use it to mark out pieces, literally **divisions** of our website to target for styling:

Add a ```<div>``` to your website.  What do you see when you reload the page?
```
<div> </div>
```
Nothing changes! We have to add content and styling to make use of the ```<div>```

Let's create another custom CSS styling class.  We will call it ```fancyStyle```.  Let's add it to our div:

```
<div class="fancyStyle"> </div>
```
Save and refresh the page.  What do you expect to see?

We have to add some styling to fancyStyle:
```
.fancyStyle{
    width: 200px;
    height: 300px;
    background: blue;
}
```

Save and refresh the page.  Now what do you see?

Experiment with other CSS properties:
```
width: 50px;
height: 50px;
background-image: url("");
border: 6px dotted purple;
border-left: 1px solid green;
```

### Project
Start building your personal webpage.
* Start with the empty HTML document
* Be sure to add a title!
* Add some headers and paragraphs.
* Add an image
* Style some elements

Stretch goals:
* Add some links
* Build some divs and do custom class styling.

### Stretch project:
* Do a search for ```CSS Flexbox```.  See if you can use this to position a ```<div>``` in interesting ways on your webpage.


### End of Class
* Submit your work!  On your desktop, create a folder with your name.  Put your work into that folder.  Drag the folder into the shared folder [here](https://drive.google.com/drive/folders/1samMDc4FVRW4sjId1NHQE8b7aCv7GGLv?usp=sharing). 

### Further Exploration
* ["Fixed mindset" vs "Growth mindset" video and discussion, Carol Dweck](https://www.ted.com/talks/carol_dweck_the_power_of_believing_that_you_can_improve)
 * View code source on some of your favorite webpages
 * FreeCodeCamp exercises: Basic HTML and HTML5, Basic CSS
* [W3Schools exercises](https://www.w3schools.com/html/exercise.asp?filename=exercise_attributes1)
