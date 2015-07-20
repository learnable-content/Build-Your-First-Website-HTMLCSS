![](headers/head3.2.jpg)
# Planning and creating markup for containers:

Now let's look at containers. The overall layout contains a series of containers inside the main rows. These containers have different widths; they're used to help centering the layout in the viewport. Some of the containers are wide, some are medium and also there is a narrow container. So we're going to use three distinct classes, `container-narrow`, `container-medium`, and `container-wide`. 

Open up *index.html* and add containers there:

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
	</div>
</div>

<!-- photos -->
<div class="row">
	photos
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
	</footer>
</div>
```

# Styling containers

Now let's style our containers. Add the following to *layout.css*.

```css
.container-narrow,
.container-medium,
.container-wide
{
	margin: 0 auto;
	padding-left: 1.5em;
	padding-right: 1.5em;
}
.container-narrow
{
	max-width: 34em;
	background: yellow;
}
.container-medium
{
	max-width: 52em;
	background: green;
}
.container-wide
{
	max-width: 58em;
	background: lime;
}
```