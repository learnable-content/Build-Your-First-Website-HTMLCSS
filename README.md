![](headers/head4.1.jpg)
# Planning the columns for the layout:

In this lesson we are going to create columns and do some clean up.

First of all, let's talk about the columns. The layout contains a series of columns and ideally, we want to create a simple grid that can then be used throughout the layout.

# Creating HTML elements for the columns

Let's mark up our columns. Open up the *index.html* file and modify it like this:

```html
<!-- banner -->
<div class="row row--banner">
  banner
  <header class="row container-wide">
    container-wide
  </header>
  <section class="row container-medium">
    container-medium
  </section>
</div>
<!-- features -->
<div class="row row--white row--padding-wide">
  features
  <div class="row container-medium">
    container-medium
    <div class="row">
      <div class="col-narrow--right">
        col-narrow--right
      </div>
      <div class="col-wide">
        col-wide
      </div>
    </div>
    <div class="row">
      <div class="col-narrow">
        col-narrow
      </div>
      <div class="col-wide--right">
        col-wide--right
      </div>
    </div>
    <div class="row">
      <div class="col-narrow--right">
        col-narrow--right
      </div>
      <div class="col-wide">
        col-wide
      </div>
    </div>
  </div>
</div>
<!-- photos -->
<div class="row">
  <div class="col-medium">
    col-medium
  </div>
  <div class="col-medium">
    col-medium
  </div>
</div>
<!-- testimonials -->
<div class="row row--white row--padding-wide">
  testimonials
  <section class="row container-narrow">
    container-narrow
  </section>
</div>
<!-- facts -->
<div class="row row--grey row--padding-wide">
  facts
  <section class="row container-narrow">
    container-narrow
  </section>
  <div class="row container-medium">
    <div class="col-narrow">
      col-narrow
    </div>
    <div class="col-narrow">
      col-narrow
    </div>
    <div class="col-narrow">
      col-narrow
    </div>
    <div class="col-narrow">
      col-narrow
    </div>
  </div>
</div>
<!-- press -->
<div class="row row--blue row--padding-medium">
  press
  <section class="row container-wide">
    container-wide
  </section>
</div>
<!-- footer -->
<div class="row row--dark-grey row--padding-medium">
  footer
  <footer class="row container-wide">
    container-wide
    <div class="col-wide">
      col-wide
    </div>
    <div class="col-narrow--right">
      col-narrow--right
    </div>
  </footer>
</div>
```
# Styling the columns

Open up *layout.css* and paste the following code:

```css
.col-narrow { background: pink; }
.col-narrow--right { background: pink; }
.col-medium { background: silver; }
.col-wide { background: aqua; }
.col-wide--right { background: aqua; }
.col-narrow,
.col-narrow--right { margin-bottom: 1.5em; }

@media (min-width: 38em)
{
	[...]

	.col-narrow,
	.col-medium,
	.col-wide { float: left; }
	.col-narrow--right,
	.col-wide--right { float: right; }
	.col-wide,
	.col-wide--right { width: 61%; }
	.col-medium { width: 50%; }
	.col-narrow,
	.col-narrow--right
	{
		width: 25%;
		margin-bottom: 0;
	}
}
```