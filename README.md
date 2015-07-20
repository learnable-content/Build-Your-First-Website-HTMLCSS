![](headers/head5.2.jpg)
# Styling the banner header area:

The next thing we need to work on is the header area that is located at the top of the page within the banner.

Open up *modules.css* and paste the following code:

```css
.header
{
	padding: 1.25em 1em;
	/* 20px/16px - 16px/16px */
}
.header__logo
{
	float: left;
	padding-top: .2em;
}
```

# Styling the banner header navigation elements

We want to push our navigation over to the right and give it a pixel width. Generally I prefer to use `em`s for sizing but just for this small screen version we need to lock it down to a pixel size:

```css
.header__nav
{
	float: right;
	width: 150px;
}
```

And now the descendants:

```css
.header__nav ul
{
  margin: 0;
  padding: 0;
  list-style: none;
  text-align: right;
}
.header__nav li
{
  display: inline-block;
  margin: 0;
}
.header__nav a
{
  display: block;
  margin-right: .2em;
  padding: 0.6em 1em 0.4em;
  border-radius: .3em;
  color: #fff;
  background: none;
  font-size: 0.8125em;
  /* 13px/16px */
  font-weight: bold;
  text-decoration: none;
}
.header__nav-contact a { margin-right: 0; }
.current a
{
  color: #fff;
  background: #56b880;
}
.header__nav a:focus { background: #000; }
.header__nav a:hover { background: #3bb2d0; }
.header__nav a:active { background: #af0000; }
```

Currently, the layout is going to break at wide screens, so let's fix that now.

# Creating banner header styles for wide screens

Employ media query for wide screen:

```css
@media (min-width: 38em)
{
  .header
  {
    padding: 2.2222em 2em;
    /* 40px/18px - 36px/18px */
  }
  .header__nav { width: 12em; }
  .header__nav a
  {
    font-size: 0.8333em;
    /* 15px/18px */
  }
}
```

Reload the page and observe the result.