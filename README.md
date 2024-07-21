# flex_gallery

This is a 30-days javascript grinding  
js30 [https://github.com/ningh98/js30]    
5. Flex Panels Image Gallery [https://github.com/ningh98/flex_gallery]

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)



## Overview

The provided HTML, CSS, and JavaScript code creates an interactive flexbox panel layout where clicking on a panel expands it and reveals additional text. This example demonstrates the use of flexbox for layout, CSS transitions for animations, and JavaScript for interactivity. 

### Screenshot

![](./screenshot1.png)
![](./screenshot2.png)

### Links

- Live Site URL: [https://ningh98.github.io/flex_gallery/]

## My process

### Built with

- HTML
- CSS
- Javascript



### What I learned


```css
.panel {
flex: 1;
justify-content: center;
align-items: center;
display: flex;
flex-direction: column;
}
.panel > *:first-child { transform: translateY(-100%)}
.panel.open-active > *:first-child {transform: translateY(0)}

```
using flex and > * to target the direct children
```js
function toggleActive(e){
    if(e.propertyName.includes('flex')){
    this.classList.toggle('open-active')
    }
}

panels.forEach(panel => panel.addEventListener('click', toggleOpen))
panels.forEach(panel => panel.addEventListener('transitionend', toggleActive))
```
transitionend event listener, and to find out what event is we could console log it to make sure we are add action on the correct thing.
