![](headers/head7.1.jpg)
# Planning and creating HTML elements for testimonials

In this lesson we will style the testimonials and facts modules. As always we'll start by styling the small screen version, and then adding media queries for the wide screen version.

Open up *index.html* and paste the following code:

```html
<div class="row row--white row--padding-wide testimonials">
  <section class="row container-narrow">
    <h3 class="testimonials__heading">
      What they are saying
    </h3>
    <img src="assets/img/avatar.jpg" alt="Robert Johnson - Avatar">
    <blockquote>
      <p class="testimonials__quote">
        <em>"Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur"</em>
      </p>
      <p class="testimonials__source">
        Robert Johnson
      </p>
    </blockquote>
  </section>
</div>
```

We are using `blockquote` to mark up block quotations. Let's go ahead and give it some styling.

# Styling testimonials

Open up *modules.css* and paste:

```css
.testimonials { text-align: center; }
.testimonials__heading
{
  margin: 0 0 1.1905em;
  /* 25px/21px */
  font-size: 1.3125em;
  /* 21px/16px */
}
.testimonials__quote
{
  margin-top: 1.5625em;
  /* 25px/16px */
}
.testimonials__source { margin: 0; }
```

# Creating tetimonials styles for wide screens:

Now the styles for widescreen:

```css
@media (min-width: 38em)
{
  .testimonials__heading
  {
    margin-bottom: 1.3235em;
    /* 45px/34px */
    font-size: 1.8889em;
    /* 34px/18px */
    font-weight: normal;
  }
  .testimonials__quote
  {
    font-size: 1.3333em;
    /* 24px/18px */
  }
  .testimonials__source
  {
    font-size: 1.1111em;
    /* 20px/18px */
  }
}
```

Go on and check that in our browser.