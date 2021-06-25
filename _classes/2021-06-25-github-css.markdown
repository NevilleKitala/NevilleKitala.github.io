---
layout: class
title:  "Introduction to Github and getting started with CSS"
date:   2021-06-24 09:06:26 +0100
pair: setup
comments: true
embed_exercise: "https://docs.google.com/forms/d/e/1FAIpQLSepF3-3obLCKaPOsaW_Bo4K_zXid0KjWqLb0dl9xpJSkPXb2g/viewform?embedded=true"
solutions: "/solutions/Assignment1.zip"

review: "https://docs.google.com/forms/d/e/1FAIpQLScfBZSY9JGxR9hw2eW4d7mIqVzl6_Q3ZIlKwdX42zgrVke1QQ/viewform?embedded=true"

conclusion: "Great. You have made a start creating your Github project and have learnt about CSS. You are basically a programmer now! Congratulations"
---


# Getting Started With Github.

<br/>

### Getting Started with CLI
In the previous class you set up your Github account. To continue with this lesson please ensure you have correctly set up a [Github](github.com) account. You will also need to install Github CLI() tools, as suggested when you first log in.

For the first half of this lesson, we will set up a Github repository, which will help us track changes to the code we write from here on out.

To get started:

1. Open up your terminal (Mac)/ command line (Windows)
1. Your terminal will open you up at the root of your main drive. you can check this by typing in `ls` and press enter. This will show you a list of all folders within the folder you are currently in: (This example shows the folder structure on a mac. Might look slightly different on windows.)

```
nevillekitala ~ % ls
Applications
Desktop
Documents
Downloads
Library
Movies
Music
Pictures
Public

```

1. For organisation sake. I will create a folder for these lessons at the root of my computer.(For windows users this is equivalent to the root of your C: Drive. You can switch to your secondary Drive(D:) using `D:`. and hit enter. this will change your current folder from C: to D:). To create a new folder, `mkdir --FOLDER NAME-- `. This is exactly the same as opening your explorer, Clicking on your (D: for windows/ Home for mac ) and creating a new folder.

1. We would like to create new files in our new projects folder. to navigate into this folder from the terminal: `cd` which means **Change directory**. So to navigate into our project folder, we would need to use the command: `cd --FOLDER NAME--`.

1. Create a new folder for Assignment 1. to do this correctly `mkdir Assignment1`. From finder you should see the structure `Project>Assignment1`. Navigate into the Assignment 1 folder.

1. We have now organised our folders for this lesson. You have also gained some experience using the terminal for basic tasks. Next we would like to make our Assignment1 folder recognisable by Github, so that all the files inside it are tracked and backup.

1. to do this we can start with our first Github command `git init`. This command should work if you have Github CLI tools installed. If it does not please review the previous lesson document. This command marks your folder as a Github folder, that will match a Github project which you will also be able to view remotely form the Github website. The output resulting should look like this: `Initialized empty Git repository in /Users/--Username--/github/project/Assignment1/.git/` or similar.

1. This is all great. However, you will need configure the folder to know where your git repository exists.

<br/>

### Your First Github Repository
1. [Create a new repository](https://docs.github.com/en/github/importing-your-projects-to-github/importing-source-code-to-github/adding-an-existing-project-to-github-using-the-command-line) on [GitHub](github.com). To avoid errors, do not initialise the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub. Name the repository Assignment1 and make it public.
  <br/>
  ![create-repo](/assets/images/repo-create.png){:class="img-responsive"}
1. Next we need to copy the URL of our newly created git repository, to connect our local Assignments folder to the one in Github. We can do this by clicking on the green Clone button on the repo's page, and copying the https link.
  <br/>
  ![create-repo](/assets/images/repo-clone.png){:class="img-responsive"}

1. back in our command line/Terminal , in our Assignment1 folder, type in the following commands, replacing `<REMOTE_URL>` with the URL you copied from Github. The first command configures your folder to synchronise its contents with the ones in Github. The second command verifies the validity of the URL you have provided.

  ```
  $ git remote add origin  <REMOTE_URL>
  $ git remote -v
  ```

1. Finally to ensure your remote repo and your local repo are communicating correctly: `git push -u origin master`. The git push, submits the changes in your local repository up to the remote repository you specified as the origin.

1. If this command succeeds, you have configured your Github repo correctly. Check your remote repository on github. We expect that nothing has changed.

Great! You have just set up your first Github repository!

## Q & A

Anything you have not understood yet?
Anything Confusing ?
Leave questions in the comment section below if an instructor is not available.

## Add files to Github:

1. This one is simple. Download the Assignment solution linked at the beginning of this doc and save it in you Assignment1 folder. Unzip the files. Then open this folder in Atom.

1. It is possible now to track what has changed in your project since the last time you did a `git push`. In your terminal, type in `git status`, which will show a list of all the files that you have added. mY output looked like:

```
nevillekitala Assignment1 % git status
On branch master

No commits yet

Untracked files:
(use "git add <file>..." to include in what will be committed)
Assignment1/
```
**Feel free to ask question here as this can all be confusing the first time around**

1. This shows that your repository has been configured correctly.

1. Back in atom you should have a folder that contains three html files and a few images in you project. Open up the index file and have a look at the webpages. Inspecting the code will show you that the webpage contains the basic structure of a HTML page including:
  - A head
  - A body
  - A header
  - content
  - A footer

This pages have no styling. Lets change that.


# CSS:

CSS stands for Cascading Style Sheets. It describes how HTML elements are to be displayed on screen, paper, or in other media. CSS saves a lot of work. It can control the layout of multiple web pages all at once
External stylesheets are stored in CSS files

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

To see this in action add the code below right before the closing `</head>` tag of the index file in you assignment1 folder.

```<style>
body {
  background-color: lightblue;
}

h1 {
  color: blue;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
</style>

```

Reload the index.html webpage in your browser. Notice anything different?
Lets breakdown the code we just wrote down.

1. the `<body>` in our code will have a `lightblue`.
1. All the `<h1>` tags in our code will be coloured `blue` applied to it.
1. All `<p>`tags in our code will have the font `verdana`.

Fun right.
The structure of HTML is pretty straight forward to begin with. You can refer to the tags you want to style by using the tag names without the angular brackets. The properties you want to style for that element are contained in curly braces. The general rule of thumb when defining a property is ` propert-name: property-value;`. This is strict and will cause errors in your styles if you do not get the syntax correct.

example:
```
selector{
property: value; #declaration
property: value; #declaration
}
```

example:

![CSS-SYNTAX](/assets/images/css_syntax.gif){:class="img-responsive"}

as explained [here](https://www.w3schools.com/css/css_syntax.asp)

Here is a [list](https://www.w3schools.com/cssref/) to all CSS properties and values that can be applied to a selector. Please spend a minute or two going through this.

As you can tell by now, CSS code can grow long overtime as more values are declared. Previously we added CSS directly into our index file. While that works OK. You would need to cope and paste it to your about.html file and your menu file so that your styles are the same. It gets worse when you want to make updates to your CSS. this is called internal CSS. While it is useful in some instances, we want to stick to external CSS. Check your menu and about pages. It is expected that the styles do not apply to them.

1. Start by creating a style.css file in the same folder as your index.html file.

1. remove all the css we copied into the index.html file, including the `<style>` tags.

1. Add this right before the closing head tag: `<link rel="stylesheet" href="styles.css">` That link just says refer to my styles.css file for all my CSS styling code.

1. Proceed to add the link into you about and menu pages.

1. copy the following styles into you CSS file:

```
body {
  background-color: lightblue;
}

h1 {
  color: blue;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

Do your styles apply across all your pages? Good.

### Coding Exercise:

For the Website Colours:
1. Change the background of the body to `#282d33`.

1. Change the colour of all Headings to `#b3885b`.

1. Change the width of all images to `50%`;

1. Change the [font](https://www.w3schools.com/css/css_font.asp) of all the text on the webpage to whatever you would like;

For the Website Spacing and layout:
1. Add a padding of `30px` to the body of the website;

1. Add a margin of `5px` after every paragraph;

1. Centre all images;

For the Styles:
1. remove decorations(underlines, different colours etc.) from all links.

1. remove list decorations from navigation.

1. Change navigation display style from `in-line` to block

**You will need to do some research from the internet to do this**

### Selectors

[Selectors](https://www.w3schools.com/css/css_selectors.asp) do what it sounds like. It selects the element you want to style. So far we have seen:

**The CSS element Selector**

The element selector selects all HTML elements based on the element name.

```
p {
  text-align: center;
  color: red;
}
```

You can apply the same styles to multiple objects by grouping selectors like:
```
p, h1, h2, h3, h5 {
  text-align: center;
  color: red;
}
```

This is great. But what happens when you want to apply styles to a specific group of paragraphs that do not apply to others?

**The CSS class Selector**

Class selectors allow us to define a custom group to which you can apply the same styles. To do this you will need to add the class attribute to your html element: `class="long"`. For example:

```
<p class="long">... </p>
```

which you would use in css as follows:

```
.long{
  #example property
  width: 100%
}
```
To select elements with a specific class, write a period (.) character, followed by the class name.

You can give the same element multiple classes, and you can give multiple elements the same class.

```

<div class="long wide tall small">... </div>

<p class="long"

<img class="long" />

```


which can be used as follows:

```

#to select all divs that have the classes long, wide and small.
#There is no space between the selectors in this case.
#This signifies that we are referring to the same element.

div.long.wide.small{
  ...
}

# to select all elements with class long
.long{
  ...
}

#to select specific paragraph with class long
p.long{

}
```

### Coding Exercise:

In the atom project tree viewer in the complete left of the screen, go to the Assignment folder containing your webpages. We would like to highlight the word juice every time it is mentioned.
1. `Mouse left click > Search in Folder`.

1. Search for the word `'juice'` and replace it with `<span class="juice"> juice </span>`. We have just replaced the word juice with a html element with a class juice applied to it.

1. in your CSS we can then apply styles to the word Juice as we see fit: you can apply your own styles to it. I recommend colouring it :`#b0544c`.

1. That all works well but what about a case where we want to have a different colour for the instances of the word `'Juice'` that appear in the heading? I will apply a different colour to the ones that appear in h1 tags as follows:

```
#Selects all elements that are children to h1 elements and have the class juice
#There is a space between the selectors in this case.
# This signifies that we are referring to children of the element.

h1 .juice{
  color: #0288cb;
}
```


**The CSS id Selector**

The id selector uses the id attribute of an HTML element to select a specific element. To do this you will need to add the id attribute to your html element: `id="long"`. For example:


```

<div id="long">... </div>

```

The id of an element is unique within a page, so the id selector is used to select one unique element!

To select an element with a specific id, write a hash (#) character, followed by the id of the element.

```
#long{
  width: 100%
}
```

# Further Reading:
1. [CSS references](https://www.w3schools.com/cssref/)
1. [CSS selectors](https://www.w3schools.com/cssref/css_selectors.asp)
1. [CSS Web safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)

# Assignment:

Using the solution from last weeks assignment, style the table from the menu page in our static website to be more colourful.

Your work will be acceptable if there is:
  1. Good use of white space
  1. Proper use of contrasting colours that are clear and readable
  1. Creative.
  1. Good use of styles and proper practices.
  1. Readability of your code.
  1. Length of your code.
  1. The amount of repetition in your style sheets.

`The Menu Page Should have:`
1. A table listing at least five menu items.
1. A picture for each item.

Feel free to use any resources from the internet.
