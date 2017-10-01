# Overview

Various CSS and CSS3 notes.

# References and Credits

* [W3 School CSS Tutorial](https://www.w3schools.com/css/default.asp)

# Positioning with Margin, Padding, etc

## Four positions provided

Example: `Margin: 10px, 5px, 15px, 20px`

Position: Top: 10px, Right: 5px, Bottom: 15px, Left 20px

## Three positions provided

Example: `Margin: 10px, 15px, 5px`

Position: Top: 10px, Left and Right: 15px, Bottom: 5px

## Two positions provided

Example: `Margin: 10px, 15px`

Position: Top and Bottom: 10px, Left and Right: 15px

## One positions provided

Example: `Margin: 10px`

Position: Top, Bottom, Left and Right: 10px

# CSS3 Flexbox for positioning

* [CSS Flexbox in 20 minutes](https://www.youtube.com/watch?v=JJSoEo8JSnc)

# Colors

## Types

* Color Names - the basic colors name red, green, blue, etc

* HTML 5 Color Names - adds a number of colors, such as coral, crimson, etc.  Along with the basic color names, there are 140 color names supported by modern browsers.

* Hexadecimal - six digit hexadecimal number (#000000 for black and #ffffff for white)

* RGB - using RGB values rgb(0, 0, 255) for blue

## CSS Color syntax

* Example for the body tag

```css
body {
    background-color: lightgray;
    color: black;
}
```

# CSS fonts

## Font Basics

* Serif fonts are the more stylize, such as Times New Roman

* Sans-Serif are the straighter blockier fonts, such as Arial

Refer to [W3 Schools CSS Font](https://www.w3schools.com/css/css_font.asp)

## Font family

* Font family example for body

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```
Evaluated from left to right.  If the left most one isn't available on the browser it tries the next

## Font size, weight

* Example for body tag

```css
body {
  font-size: 20px;
  font-weight: normal; /* bold, etc */
}
```

## Shortcut (combined) font syntax

* Example Weight, size, and family combined for body tag

```css
body {
  font: normal 20px Arial, Helvetica, sans-serif;
}
```

## Line height

* Increase the line height over the standard 1em height which gives more line spacing

```css
body {
    line-height: 1.6em
}
```

# Classes and Ids

## General

* Use Ids for unique identication of elements

* Use Classes for groups of elements

* Use .classname notation for classes in CSS

```css
.container {
    width: 500px;
    margin: auto;
}
```

* use #id notation for Ids in CSS

#pageheading {
    font-size: 20px;
    color: blue;
}

# Extending CSS with Sass/Less

Allows the adding of programming logic such as variables and conditionals
