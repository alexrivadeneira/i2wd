# Intro to Web Dev

Welcome to Class!

## Week 2 Outline

### As you come in:
* Navigate to nerdyperson.com (this page!)
* One more survey question for you! [survey](https://goo.gl/forms/YLKsi1OeHUjGi2pQ2)
* Complete the warmup exercise:

### Warmup Exercise

* Open the Sublime application on your computer (if you can't find Sublime, click the Windows icon in the lower left hand corner of the page.  In the text box that appears, type Sublime.  You should see Sublime appear in the applications list).
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
* Save the file.  Select Save


### Sublime
Sublime is code editing program.  Most importantly, Sublime provides **syntax highlighting** meaning it adds color to our code to help us visualize its structure.  **Syntax** refers to the structure of our code and the rules that govern that structure.  

**Can you remember some rules about HTML code from last class?**
Review: Where is HTML nested in our HTML document?
```
<h1> My header </h1>
<h1 class="fancyStyle"> My styled header</h1>

```
**What about CSS syntax?**
Review: Where is CSS nested in our HTML document?
```
h1{
    background: green;
    color: white;
    margin: 15px;
}
```
Sublime can help us catch small syntax errors that we would otherwise have to search for ourselves.

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


### End of Class
* Submit your work!  On your desktop, create a folder with your name.  Put your work into that folder.  Drag the folder into the shared folder [here](https://drive.google.com/drive/folders/1samMDc4FVRW4sjId1NHQE8b7aCv7GGLv?usp=sharing). 

### Further Exploration
* ["Fixed mindset" vs "Growth mindset" video and discussion, Carol Dweck](https://www.ted.com/talks/carol_dweck_the_power_of_believing_that_you_can_improve)
 * [FreeCodeCamp exercises](https://www.freecodecamp.org): “Front End Development Certifications” > “HTML5 and CSS” – complete all of the exercises there (through “Use RGB to Mix Colors”)