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
* Helpful previous knowledge: high school algebra, basic computer skills like navigating websites
* Thursdays at 10 AM is a [beginner computer class](https://www.berkeleypubliclibrary.org/events/beginner-computer-class-central-ec-0)  
* Attend all five sessions, submit classwork to earn certificate from the library.

### Class goals
* Transition from web consumer to producer/maker/creator
* Build some fun projects: personal website, interactive game
* Build foundation so you can keep learning on your own

### Changing perspective from web content consumer to producer
* "Peek behind the curtain" with Chrome developer tools.  Right click: "View Page Source"
* Set up your first html file.  In Notepad, select File > Save As.  Save your file as anything.html 
* Notice, this file isn't a text file anymore! Now it's a website file (HTML file)

### HTML Tags
* HTML tags are the building blocks of websites.  Most tags have an opening and closing tag that you can put stuff between (**nesting**).

This is an opening and closing header tag:
```
<h1> </h1>
```

We can put text between the tags to make a header for our website:  
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
You can add properties and data called **attributes** to further customize some tags.  Here's a tag to add an image to your website:
```
<img> </img>
```

We need to pass an image source (src) to the tag so it can render an actual picture:

```
<img src="mypicture.png"> </img>
```

If you find an image you like, right click and select "Copy image address".  This will copy the source/location of your image for you.

⚠️ 🚨 ** Be careful with formatting!  Watch for opening and closing carets and quotation marks! **

Here's how to create a link using the ** anchor ** tag and the ** href ** attribute.

```
<a href="http://www.google.com">Link to Google</a>
```

### Nesting HTML Tags
You've already nested text nodes inside of HTML tags.  Now let's try nesting some HTML tags inside of other tags!

These tags in combination make make an unordered list.  Notice how the ```li``` tags are nested inside the outside ```ul``` tags:
```
<ul>
    <li>Apples</li>
    <li>Quinoa</li>
    <li>Spaghetti</li>
<ul>
```



### End of Class
* Submit your work!  On your desktop, create a folder with your name.  Put your work into that folder.  Drag the folder into the shared folder [here](https://drive.google.com/drive/folders/1samMDc4FVRW4sjId1NHQE8b7aCv7GGLv?usp=sharing). 

### Further Exploration
* ["Fixed mindset" vs "Growth mindset" video and discussion, Carol Dweck](https://www.ted.com/talks/carol_dweck_the_power_of_believing_that_you_can_improve)
 * View code source on some of your favorite websites
* [W3Schools exercises](https://www.w3schools.com/html/exercise.asp?filename=exercise_attributes1)
