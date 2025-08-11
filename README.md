# Frontend Mentor - FAQ accordion solution

This is a solution to the [FAQ accordion challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-wyfFdeBwBz). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

-  [Overview](#overview)
   -  [The challenge](#the-challenge)
   -  [Screenshot](#screenshot)
   -  [Links](#links)
-  [My process](#my-process)
   -  [Built with](#built-with)
   -  [What I learned](#what-i-learned)
   -  [Useful resources](#useful-resources)
-  [Author](#author)

## Overview

### The challenge

Users should be able to:

-  Hide/Show the answer to a question when the question is clicked
-  Navigate the questions and hide/show answers using keyboard navigation alone
-  View the optimal layout for the interface depending on their device's screen size
-  See hover and focus states for all interactive elements on the page

### Screenshot

![desktop](<screenshot/faq - desktop.png>)
![desktop - active](<screenshot/faq - desktop - active.png>)
![mobile](<screenshot/faq - mobile.png>)

### Links

-  Solution URL: [Add solution URL here](https://your-solution-url.com)
-  Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

-  Semantic HTML5 markup
-  CSS custom properties
-  Flexbox
-  CSS Grid
-  Mobile-first workflow

### What I learned

1. Animating height:auto alternative - Since we can't animate height: auto (unless we use interpolate-size: allow-keywords, caveat is limited browser support). Instead of animating the height itself, create a container with display:grid, then animate the grid-template-rows from 0fr to 1fr.

```html
<div class="parent">
  <input type="checkbox" name="" id="">
  <h2>Q1</h1>
  <div class="container">
  <p class="content">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ad, mollitia. Iure nam voluptatem saepe dolorum culpa vero ipsa, inventore veritatis.</p>
  </div>
  <h2>Q2</h2>
</div>
```

```css
input:checked ~ .container {
   grid-template-rows: 1fr;
}

.container {
   display: grid;
   grid-template-rows: 0fr;
   transition: grid-template-rows 0.25s linear;
}

.content {
   overflow: hidden;
}
```

### Useful resources

-  [Animate height:auto - alternative](https://marcsamtleben.de/de/blog/animate-height-auto-with-pure-css) - The alternative solution is to animate the grid-template-rows from 0fr to 1fr.

## Author

-  GitHub - [AJ-Tan](https://github.com/AJ-Tan)
-  Frontend Mentor - [@AJ-Tan](https://www.frontendmentor.io/profile/AJ-Tan)
