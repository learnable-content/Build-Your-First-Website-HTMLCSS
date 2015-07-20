![](headers/head7.2.jpg)
# Planning and creating HTML elements for facts area:

For the facts area we need to focus on a range of different areas. The first one is the actual facts container. Inside it there is the facts intro heading and the facts intro text. Then we have a series of list items, list heading, list text, and list icon. Inside this we have an ID, and eye, a timer, and a chart images.

As always, we'll be focusing on narrow screen first and then proceed to wide screen version.

Open up *index.html* and paste the following code:

```html
<div class="row row--grey row--padding-wide facts">
  <section class="row container-narrow facts-intro">
    <h3 class="facts-intro__heading">
      A few facts
    </h3>
    <p class="facts-intro__text">
      Lorem ipsum dolor sit amet, consectetur adipiscing metus elit.
    </p>
  </section>
  <div class="row container-medium facts-list">
    <div class="col-narrow">
      <span class="facts-list__icons facts-list__id"></span>
      <h4 class="facts-list__heading">2,000,000</h4>
      <p class="facts-list__text">Lorem ipsum</p>
    </div>
    <div class="col-narrow">
      <span class="facts-list__icons facts-list__eye"></span>
      <h4 class="facts-list__heading">11,000,000</h4>
      <p class="facts-list__text">Lorem ipsum</p>
    </div>
    <div class="col-narrow">
      <span class="facts-list__icons facts-list__timer"></span>
      <h4 class="facts-list__heading">5 minutes</h4>
      <p class="facts-list__text">Lorem ipsum</p>
    </div>
    <div class="col-narrow">
      <span class="facts-list__icons facts-list__chart"></span>
      <h4 class="facts-list__heading">40%</h4>
      <p class="facts-list__text">Lorem ipsum</p>
    </div>
  </div>
</div>
```

# Styling facts intro area:

Open up *modules.css* and paste:

```css
.facts { text-align: center; }
.facts-intro__heading
{
	margin: 0 0 .3em;
	font-size: 1.5625em;
	/* 25px/16px */
}
.facts-intro__text
{
	margin: 0 0 2em;
	/* 32px/16px */
}
```

# Styling facts lists area

Next paste styles for facts lists area:

```css
.facts-list__heading
{
  margin: 0 0 .25em;
  /* 4px/16px */
  font-size: 1.5em;
  /* 24px/16px */
  font-weight: bold;
}
.facts-list__text { margin: 0; }
```

# Styling facts icons area

Styles for facts icons area:

```css
.facts-list__icons
{
  display: block;
  width: 70px;
  height: 44px;
  margin: 0 auto 1.3333em;
  /* 24px/16px */
  background-repeat: no-repeat;
  background-image: url(../img/icon-sprite.png);
}
.facts-list__id { background-position: 0 0; }
.facts-list__eye { background-position: 0 -44px; }
.facts-list__timer { background-position: 0 -88px; }
.facts-list__chart { background-position: 0 -132px; }
```

# Creating facts styles for wide screens

Now we need another media query for widescreen:

```css
@media (min-width: 45em)
{
  .facts-intro__heading
  {
    font-size: 1.8889em;
    /* 34px/18px */
    font-weight: normal;
  }
  .facts-intro__text
  {
    margin: 0 0 2.5em;
    /* 50px/20px */
    font-size: 1.1111em;
    /* 20px/18px */
  }
  .facts-list__heading
  {
    font-size: 1.5556em;
    /* 28px/18px */
  }
}
```

Reload the page in your browser to check that fact areas and icons are now working.