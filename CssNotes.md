# Overview

Various CSS and CSS3 notes.

# References and Credits

* [W3 School CSS Tutorial](https://www.w3schools.com/css/default.asp)

# CSS Selectors

**CSS** consists of **Selectors** followed by **Declaration blocks**.  There are several types of **selectors**

* Element Selector
* ID Selector
* Class Selector
* Descendent Selector
* Universal Selector
* Child Selector
* Attribute Selector

## Element Selector

**Element selectors** use the **element name**

```css
p {
    color: black;
}
```

## ID Selector

**ID selectors** use the elements **id** preceeded by a **hash \#**

```css
#myId {
    font-weight: bold;
    background-color: aqua;
}
```

## Class Selector

**Class selectors** apply to an elements **class attribute** proceeded by a **period .**

```css
.leftsidebar {
    height: 100%;
    width: 15%;
    ...
}
```

## Descendent Selector

**Descedent selectors** apply only to the **specified element** name contained **within the parent element**.  For example the following will only appy to an **input** element within a **form** element, but not an **input** element outside of a **form**.

```css
form input {
    width: 50%;
}
```

## Universal Selector

**Universal selectors** is used to select the name of **all element types** using an **asterisk \***

```css
* {
    color: blue;
}
```

## Child Selector

**Child selectors** select an element only if it is a **direct child** of another element.  The following affects all **paragraphs** directly under the **body** element, but would not effect a **paragraph** that is further nested under another element such as **div**:

```css
body>p {
    color: blue;
}
```

## Attribute Selector

**Attribute selectors** selects elements with **specific attributes**:

```css
input[type="text"] {
    color: blue;
}
```

## Grouping Selectors

You can apply the same styles to multiple elements by **group selectors** together, **separating them with commas**:

```css
h1, h2, h3, h4 {
    color: blue;
}
```

## Pseudo Elements

**Pseudo elements** are used to style specific parts or several parts of HTML elements.  They allow you to add special effects to certain elements.  Common pseudo elements include:

* **:first-line**
* **:first-letter**
* **:before**
* **:after**

For example:

```css
p:first-letter {
    color: blue;
    font-size: x-large;
}
```

# Cascading Order

When you define multiple styles, all styles will **cascade** into a new virtual style sheet in the following order of priority:

* Inline Styles
* External and Internal Stylesheets defined in the **head** section of the **HTML**
* Default **Browser Styles**

# Positioning

## Margin and Padding

* Margin adds space to the outside of the element, padding adds space to the inside. The border is between the margin and the padding.
* The `margin:auto` notation places an equal size to the left and right margins

    ```css
    body {
        width: 80%;
        margin: auto;
    }
    ```
This will center the content, with 10% for the left margin and 10% for the right margin

* For no margin and no padding specify 0 without a unit

    ```css
    body {
        margin: 0;
        padding: 0;
    ```

## Margin and padding explicit notation

* Example with margin, the same applies to padding

    ```css
    body {
        margin-top: 5px;
        margin-bottom: 5px;
        margin-right: 10px;
        margin-left: 10px;
    }
    ```

## Margin shortcut (combined) notation (also applies to padding)

### Four positions provided

Example: `Margin: 10px, 5px, 15px, 20px`

Position: Top: 10px, Right: 5px, Bottom: 15px, Left 20px

### Three positions provided

Example: `Margin: 10px, 15px, 5px`

Position: Top: 10px, Left and Right: 15px, Bottom: 5px

### Two positions provided

Example: `Margin: 10px, 15px`

Position: Top and Bottom: 10px, Left and Right: 15px

### One positions provided

Example: `Margin: 10px`

Position: Top, Bottom, Left and Right: 10px

## CSS3 Flexbox for positioning

* [CSS Flexbox in 20 minutes](https://www.youtube.com/watch?v=JJSoEo8JSnc)

# Colors

## Types

* Color Names - the basic colors name red, green, blue, etc
* HTML 5 Color Names - adds a number of colors, such as coral, crimson, etc.  Along with the basic color names, there are 140 color names supported by modern browsers.
* Hexadecimal - six digit hexadecimal number (#000000 for black and #ffffff for white).  There is also an abbreviated 3 digit notation.
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

* Use Ids for unique identification of elements
* Use Classes for groups of elements
* Use .classname notation for classes in CSS

    ```css
    .container {
        width: 500px;
        margin: auto;
    }
    ```

* use #id notation for Ids in CSS

    ```css
    #pageheading {
        font-size: 20px;
        color: blue;
    }
    ```

## Targeting elements within a class

* Target the h1 element within the container class.  This will not affect h1 elements outside the scope of this class

    ```css
    .container h1 {
        color: blue;
    }
    ```

* Multiple elements can be targeted

    ```css
    .container h1, .container h2, .container h3 {
        color: blue;
    }
    ```

## Targeting a specific type of **input** element within a form group named **my-form**

* Targeting the **text** type of **inputs**

    ```css
    .my-form input[type="text"] {
        padding: 8px;
        width: 100%
    }
    ```
    Since this only targets the text type of inputs, we can stretch these to 100% of the container, without the submit type of input buttons also being stretched to 100%.

# Element States

* Some elements such as an anchor `<a>` can have a state (hover, active, visited, etc) that you can target with element:state notations.  For example:

    ```css
    a:hover {
        color: red;
    }

    a:active {
        color: blue;
    }

    a:visited {
        color: green;
    }
    ```
# Extending CSS with Sass/Less

Allows the adding of programming logic such as variables and conditionals
