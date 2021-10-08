# Frontend Mentor - Time tracking dashboard solution

This is a solution to the [Time tracking dashboard challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/time-tracking-dashboard-UIQ7167Jw). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Extra challenges](#extra-challenges)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size.
- See hover states for all interactive elements on the page.

### Extra challenges

As a bonus I want to achieve the following extra challenges:

- The page must be accessible according to WCAG 2.1 standards, things like color contrast, clear element focus and necessary aria attributes.
- I want to add minimal animations to the page, such as a starting animation when the page loads and hover animations on the category cards.
- I took on the extra challenge of using the data from the data.json file and displaying it according to whether the user is viewing daily, weekly or monthly stats.

### Screenshot

![social-preview-image](https://user-images.githubusercontent.com/3909046/136522531-a94558cb-0cb2-431a-8518-66fb0bab9442.png)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/)
- [Live Site URL](https://markteekman.github.io/time-tracking-dashboard/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- WCAG 2.1 best practices
- CSS Animations
- JavaScript Fetch API
- [Astro](https://astro.build) - Astro Static Site Generator
- [Accessible Astro Starter](https://github.com/markteekman/accessible-astro-starter) - My own starter template for Astro

### What I learned

- I learned that when adding transforms on an element, it creates its own [stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context). I wanted to add a fade-in animation on my dashboard cards. The cards have a background with an icon in the `::after` pseudo element and are stacked behind the card using `z-index: -1;`. However, when you use a transform on the element it creates its own stacking context, causing the z-index position not to work as expected. A solution for this is to wrap the element containing the `::after` pseudo element in a container and apply the transform there so that your original stacking context is not changed. This [Stack Overflow solution](https://stackoverflow.com/questions/20851452/z-index-is-canceled-by-setting-transformrotate) describes it in great detail.
- I learned how to get data from a `.json` file and display it on the page depending on which data the user wants to see. I used the JavaScript Fetch API to make this work.

### Continued development

- I could maybe add an extra grid view for tablet sizes, with the category cards two by two and the user card spanning three rows.

### Useful resources

- [Stacking contexts and z-index](https://stackoverflow.com/questions/20851452/z-index-is-canceled-by-setting-transformrotate) - The solution I applied for using transforms on elements that have a negative z-index positioned `::after` pseudo element.
- [JavaScript Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) - Used to get the data from the `.json` file.

## Author

- [Personal Website](https://www.markteekman.nl)
- [Frontend Mentor Profile](https://www.frontendmentor.io/profile/markteekman)
- [LinkedIn Page](https://nl.linkedin.com/in/markteekman)
- [GitHub Projects](https://github.com/markteekman)
- [NPM Packages](https://www.npmjs.com/~markteekman)
- [CodePen Creations](https://codepen.io/markteekman)
