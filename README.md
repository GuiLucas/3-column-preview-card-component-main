# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./images/screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://guilucas.github.io/3-column-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid

### What I learned

I was not able to get the border radius propriety for the container of all the cards because the ```html <div class="card"></div>``` on top of it was overflowing. At first tried to give each card a custom border only on top left and bottom left but found that we can use ```css overflow: hidden; ``` as best practice.

Instead of changing every button font-color for each card, that would create code repetion, I found that we can use the following propriety to have the same color background of the parent element:

```css
.button{
  mix-blend-mode: screen;
}
```

I wanted to animate the hover propriety of the button, but also wanted to have animation for when the mouse leaves the button. This could be done with JavaScript, however, I did it with 2 keyframes animations. However, it might be nicer to implement this on JavaScript as the animation happens on load and it should only animate back when the mouse exits the button.

```css
@keyframes paint {}
@keyframes disolve {}
}
```

I wanted to animated the icons of each card to dropIn, one at a time. This was a good example to apply the tip I saw on [Fireship video on CSS tricks](https://www.youtube.com/watch?v=Qhaz36TZG5Y&). You can usee CSS Variables and the function calc() on animation-delay to do this without repeating code.

```html
<div class="icon" style="--order: 1">
```

```css
.icon {
  animation-delay: calc(var(--order) * 100ms);
}
```

### Useful resources

- [Fireship video on CSS tricks](https://www.youtube.com/watch?v=Qhaz36TZG5Y&) - Discovered how powerfull CSS variables and calc() function works together for not repeating code. See section above - [What I learned](#what-i-learned) 

## Author

- Website - [Guilherme Lucas](https://www.guilhermelucas.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/guilucas)
