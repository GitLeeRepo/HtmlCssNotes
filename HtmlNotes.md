# Overview

Notes on HTML, with HTML5 being emphasised.  Note meant to be an in-depth list of HTML elements, but simply noting a few things.  Refer to the References for a more in-depth list of HTML features and elements

# References

* [W3 Schools HTML tutorial](https://www.w3schools.com/html/html5_intro.asp)

# Tips and Tricks

## Links

* To have a link (typically external) open in a new browser tab add the `target="_blank"` attribute to the anchor `<a>` element.  For example:

  ```html
  <a href="https://www.w3schools.com/html/html5_intro.asp" target="_blank">W3 Schools HTML 5</a><br>
  ```

# HTML Editors

## Visual Studio 2017

By default Visual Studio uses XHTML syntax for closing tags, e.g. `<br />` rather than HTML 5 which doesn't require this for tags that don't have inner HTML content, so `<br>` is preferred.  To change this default:

* Navigate on the menu to **Tools/Options**
* Select **Text Editor/HTML/Advanced** from the options
* Under **Completion** set **XHTML Coding Style** to **False**

## Visual Studio Code

