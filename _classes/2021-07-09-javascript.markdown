---
layout: class
title:  "Introduction to CSS Bootstrap and Basic Javascript"
date:   2021-07-09 09:06:26 +0100
comments: true
solutions: "/solutions/Assignment2.zip"

review: "https://docs.google.com/forms/d/e/1FAIpQLScfBZSY9JGxR9hw2eW4d7mIqVzl6_Q3ZIlKwdX42zgrVke1QQ/viewform?embedded=true"

conclusion: "Great. Javascript is a widely used coding languages with plenty of resources around the web. it would be prudent to put some time into using it to modify the website in your past time."
---



# Bootstrap with CSS:
## What is Bootstrap:

[**Bootstrap**](https://en.wikipedia.org/wiki/Bootstrap_(front-end_framework)) : Bootstrap is a free and open-source CSS framework directed at responsive, mobile-first front-end web development. It contains CSS- and (optionally) JavaScript-based design templates for typography, forms, buttons, navigation, and other interface components.

In other words it gives you a Library of compiled css styles that you can link into your webpage and link to your changes as you please. This makes it easier for developers to maintain a consistent style through out their designs.

## Exercise 1:
1. Extend the solution from the previous week to include bootstrap styles by.

  1. change the background colour of the navigation bar to use bootstrap.
  1. Change the table to a grid of cards, which should show the image, the price and a short description of the different juices.
  1. Every time the word <em>juice</em> is mentioned, colour it green.
  1. Every time the word <em> Natalie'e </em>
  make use of containers from bootstrap to replace the text class used for divs in the solution.

# Javascript:
## What is javascript:

**Javascript** is a programming language that adds interactivity to your website. **interactivity** refers to  a way of communicating with the user of your website. An interactive website includes elements which can be actively engaged by the user and therefore provides better user experience in the behaviour of responses when buttons are pressed or with data entry on forms; with dynamic styling; with animation, etc.

JavaScript ("JS" for short) is a full-fledged dynamic programming language that can add interactivity to a website. It was invented by Brendan Eich (co-founder of the Mozilla project, the Mozilla Foundation, and the Mozilla Corporation).

### Adding Javascript to you website:
1. Go to your website folder from the previous assignment. Feel free to also use the solution provided above.
1. Create a new folder named `scripts`. Within the scripts folder, create a new file called `main.js`, and save it.
1. In your `index.html` file, enter this code on a new line, just before the closing </body> tag:

  ```
  <script src="scripts/main.js"></script>
  ```

<em>Explanation:</em>  This is doing the same job as the <link> element for CSS. It applies the JavaScript to the page, so it can have an effect on the HTML (along with the CSS, and anything else on the page).

let us add this code into the javascript file:
```

const h1 = document.querySelector('h1');
h1.textContent = 'Replacing the headings in the website!';

```

## What did you observe
We should see a `h1` in the index page changed to`Replacing the headings in the website!`.
using a function called querySelector(), you have grabbed a reference to a h1 tag and stored it in a variable called h1.

This is similar to what we did using CSS selectors. When you want to do something to an element, you need to select it first.

Following that, the code set the value of the myHeading variable's textContent property (which represents the content of the heading) to Hello world!.

great. You have just got started writing your first bit of javascript.

Now for a quick [crash course](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics):

### Exercise 2
We are going to change the background image of the intro section of our landing page.

 1. Using what you have learn:
  1. Find where the image is selected defined.
  1. Start by trying to reference the image/ image container in a variable in our javascript
  1. You can find all images in the Assets folder of the solution for last weeks assignment. Find the name of the image you want to replace our background with, and save its location in a variable as well.
  1. replace the image using javascript.

## Assignment
If you were able to successfully finish the previous exercise
  1. for bonus points, replace the background image from the previous exercise with a new image every 10 seconds.

# Further Reading:
1. [Bootstrap](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
1. [Getting started with javascript](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#adding_a_personalized_welcome_message)
