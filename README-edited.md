# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./03screenshot_desktop.png)


### Links

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid

### What I learned

1. Hovering the parent element --> change apply on child element

example code: 
```html
<div class="container">
   <div class="item">
     font color changes if container was hovered.
  </div>
</div>
```

```css
.container:hover .item {
  color: cyan;
}
```

https://stackoverflow.com/questions/10769016/display-image-on-text-link-hover-css-only

I still wonder if the hover effect could affect the other div (not parent one), it turns out that the effects could apply on the one selector can reach to.
https://stackoverflow.com/questions/6910049/on-a-css-hover-event-can-i-change-another-divs-styling

2. try to set transition duration to the position absolute changes

First, the transition was set under body, as I would like to apply to all of the hover effect.
But I found all of them not working. Turns out they transition is **NOT** inherit property.
If I want them working on everything, the best way is applying to * selector.
If there are specific element that I want to apply on, transition should be added on according element.

https://www.w3schools.com/cssref/css3_pr_transition.asp


3. add in the border (horizontal line) without using border of div

```html
<!-- new tag that I have not used before -->
<hr>
```
https://www.w3schools.com/tags/tag_hr.asp

4. Margin-top in div > h1 not expanding the div but adding on div's margin?

The reason should collapsing margin (which I am totally unfamiliar with):

_"In simple terms, this definition indicates that when the *vertical margins of two elements are touching*, only the margin of the element with the *largest margin* value will be honored, while the margin of the element with the smaller margin value will be collapsed to zero..._

In my words, 2 elements with their top/bottom margin touching each other, they will be seen as 1 margin and only the larger one wins. That is why the margin applies on parent div.

Answer:https://stackoverflow.com/questions/20689575/css-margin-top-of-h1-affects-parents-margin

More examples here: https://www.sitepoint.com/collapsing-margins/

Solution: _As discussed earlier, the simplest way to stop the margin collapse from occurring is to add padding or borders to each element._

OR

What I did is simply using grid/ flex

https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwijxoH9jPL1AhXAQ_UHHTtIBMgQFnoECAwQAw&url=https%3A%2F%2Fwww.smashingmagazine.com%2F2019%2F07%2Fmargins-in-css%2F&usg=AOvVaw3gzU167WtPyOTDUyFq6VP3

### Continued development

Would like to find other way to centralize the card and place the card in the bottom

## Author

- Frontend Mentor - [@Ma1021](https://www.frontendmentor.io/profile/Ma0121)

