![](headers/head4.2.jpg)
# Cleanup CSS styles

As we've been marking up our rows, columns and containers, we've been using fake background colors just so we can see what's going on. Now we're ready to style some of these components in more detail and remove those fake background colors.

Open up *layout.css* and remove the following lines:

```css
.row--banner { background: #aaa; }

background: yellow; // from .container-narrow

background: green; // from .container-medium

background: lime; // from .container-wide

.col-narrow { background: pink; }
.col-narrow--right { background: pink; }
.col-medium { background: silver; }
.col-wide { background: aqua; }
.col-wide--right { background: aqua; }
```

Now we're ready to get into some more detailed styling.