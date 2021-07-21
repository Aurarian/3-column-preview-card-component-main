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
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview
Started on 7/14
Mobile design finished on 7/16
Desktop design finished on 7/21
Finished on 7/21

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Mobile](images/finished_mobile.png)
![Desktop](images/finished_desktop.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow

### What I learned

- Learned how to vertically align using min-height: 100vh and flexbox.
- Learned how to adjust misaligned content due to height issues by nesting flex containers and using flex property
- Learned a way to get rid of movement by buttons during hover by adding a transparent border of 1px in regular state that would shift to non-transparent border when hovered/focused on

```css

main {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.sedan_card,
.suv_card,
.luxury_card {
    padding: 2em 1.5em;
    color: white;
    display: flex;
    flex-direction: column;
    /* packs all the items flush to left, prevents buttons from stretching all the way*/
    align-items: flex-start;
}

  .card_content {
    /*flex: 1 is equal to flex: 1 1 0 where grow and shrink are set to 1 and basis is set to 0
     Paragraphs won't cause misalignment shifts between cards by allowing card-content (paragraphs)
     to grow evenly.  A margin-bottom: auto would also work here. */
    flex: 1;
  }
}
.card_button {
  background-color: white;
  padding: 1em 2em;
  border-radius: 100px;
  display: inline-block;
  /* adding a transparent border to the button and then adding a
  non-transparent border on the hover/focus states allows for no
  visible movement shift to occur when hovered/focused */
  border: 1px solid transparent;
  transition: background-color, color, border 0.2ms;
}

.card_button:hover,
.card_button:focus {
  background-color: transparent;
  color: white;
  border: 1px solid white;
}
```

### Continued development

Skills I would like to continue developing:

- Continue using flexbox to get better at manipulating and identifying issues caused when using it
- General debugging
- Using more varied CSS properties
- Implementing grid instead of Flexbox
- Using markdown

### Useful resources

Thanks to [Kevin Powell discord community](https://discord.gg/KYDcWvPv) for helping me get past roadblocks.
This [stackoverflow thread](https://stackoverflow.com/questions/37386244/what-does-flex-1-mean) on flex: 1 was somewhat helpful.

## Author

- Frontend Mentor - [@aurarian](https://www.frontendmentor.io/profile/Aurarian)
