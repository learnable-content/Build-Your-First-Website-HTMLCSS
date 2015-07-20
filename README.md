![](headers/head3.1.jpg)
# Planning rows and CSS classes for website

In this lesson we will set up the rows and the containers.

Our layout contains a series of **rows** that either wrap around entire sections of the layout, or reside inside sections of the layout. We have a separate row for the header, the feature, the images, the testimonials, the recent press and the footer. Inside we also have a bunch of smaller rows which wrap around different parts of the page.

Many of the outer rows seem to be unique: they've got different padding, background colors, and even different text styles. In these cases, we could give each row additional modifier classes that can then be used to style individual characteristics.

Let's start with different background colors. There are four individual types of rows:

* row--white
* row--grey
* row--blue
* row--dark-grey

Some of the rows have different padding. You'll see that in some cases the top and bottom padding is wide, and sometimes it is more narrower. There are also special cases like the banner, and we could use a unique modifier, something like `row--banner`. So all of our classes would be things like `.row` for our module, and then we have modifiers: `--white`, `--blue`, `--dark-grey`, and `--grey`. We then have our padding modifiers: `--padding-medium`, and `--padding-wide`. We also have our special one of `--banner`. As you can see, at a glance we can immediately tell that they're all related to the row module, and that they have modifiers.

# Creating the HTML elements for rows

Open up the *index.html* file. We're going to create the markup for our rows:

```html
	<!-- banner -->
	<div class="row row--banner">
		banner
	</div>

	<!-- features -->
	<div class="row row--white row--padding-wide">
		features
	</div>

	<!-- photos -->
	<div class="row">
		photos
	</div>

	<!-- testimonials -->
	<div class="row row--white row--padding-wide">
		testimonials
	</div>

	<!-- facts -->
	<div class="row row--grey row--padding-wide">
		facts
	</div>

	<!-- press -->
	<div class="row row--blue row--padding-medium">
		press
	</div>

	<!-- footer -->
	<div class="row row--dark-grey row--padding-medium">
		footer
	</div>
```

# Styling the rows

Open up *layout.css*. The first thing we need to do is style the main row.

```css
.row
{
	clear: both;
	overflow: hidden;
}
```

`clear: both` means that the rows will clear any row above. `overflow: hidden` means that the rows will wrap around any floated items inside.

Next up are the colors.

```css
.row--white { background: #fff; }
.row--grey { background: #f8f8f8; }
.row--blue { background: #3bb2d0; }
```

Let's also set our row banner.

```css
.row--banner { background: #aaa; }
```

Now padding:

```css
.row--padding-medium
{
	padding-top: 2.1875em;
	padding-bottom: 2.1875em;
	/* 35px/16px */
}

.row--padding-wide
{
	padding-top: 2.1875em;
	padding-bottom: 2.1875em;
	/* 35px/16px */
}
```

# Adding media queries for rows

```css
@media (min-width: 38em)
{
	.row--padding-medium
	{
		padding-top: 3.8889em;
		padding-bottom: 3.8889em;
		/* 70px/18px */
	}
	.row--padding-wide
	{
		padding-top: 5.5556em;
		padding-bottom: 5.5556em;
		/* 100px/18px */
	}
}
```

This means that all the rules inside the `@media (min-width: 38em)` will only take place if the viewport is a minimum of `38em`.