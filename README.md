![](headers/head2.1.jpg)
# Review file struture of site and functionality

In this lesson we are going to look at folders, files and images.

First of all, let's review our folders. The main folder is called the *assets* and resides in the root of our directory. Inside there are folders called *css*, *img* and *js*.

The *css* folder includes the following files:

* *base.css* - base styles such as element selectors (`h1`, `blockquote`, `table`, etc).
* *layout.css* - defines the overall grids and layout components.
* *modules.css* - reusable, modular parts of the design (callouts, sidebar sections, product lists, navigation etc).
* *normalize.css* - makes browsers render all elements more consistently and in line with modern standards.

For our CSS files we're going to follow the **SMACSS principle** which breaks CSS files down to base, layout, modules, states, and themes (themes and states won't be used in the course).

Next up is the *img* folder that is holding all of our images, as well as the Apple touch icons.

The *js* (JavaScript) folder contains:

* *html5.js* - **HTML5Shiv** that enables us to style HTML5 elements in Internet Explorer 8 and below, as these versions don't allow unknown elements to be styled without JavaScript.
* *respond.min.js* - lightweight polyfill that forces Internet Explorer versions 6 to 8 to support min and max width CSS3 media queries.

# Introduction to CSS media queries

If you never heard of them before, **media queries** are an extension to the CSS2 media types. They give us much more control over how we deliver CSS to different devices. For example:

```css
@media (min-width: 38em) {}
```

This rule would be applied by any device that has a minimum viewport width of `38em`.