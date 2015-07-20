![](headers/head8.1.jpg)
# Planning and creating HTML elements for press area

In this lesson we will style the press and the footer modules.

Paste the following code into *index.html*:

```html
<div class="row row--blue row--padding-medium press">
  <section class="row container-wide">
    <h3 class="press__heading">
      Recent press
    </h3>
    <div class="row">
      <div class="press__logos press__logos--solvable">
        <a href="#"><img src="assets/img/logo-solveable.png" alt="Solveable"></a>
      </div>
      <div class="press__logos press__logos--nc">
        <a href="#"><img src="assets/img/logo-nc.png" alt="NC"></a>
      </div>
      <div class="press__logos press__logos--waratah">
        <a href="#"><img src="assets/img/logo-waratah.png" alt="The Waratah Post"></a>
      </div>
      <div class="press__logos press__logos--bevel">
        <a href="#"><img src="assets/img/logo-bevel.png" alt="The Bevel"></a>
      </div>
    </div>
  </section>
</div>
```

# Styling press area:

Paste the following styles into *modules.css*:

```css
.press { text-align: center; }
.press__heading
{
  margin-bottom: 1em;
  /* 25px/25px */
  color: #fff;
  font-size: 1.5625em;
  /* 25px/16px */
}
.press__logos { margin-bottom: 2em; }
.press__logos--bevel { margin-bottom: 0; }
```

# Creating press styles for wide screens:

And now styles for widescreen:

```css
@media (min-width: 38em)
{
  .press__heading
  {
    font-size: 1.8889em;
    /* 34px/18px */
    font-weight: normal;
  }
  .press__logos
  {
    float: left;
    margin: 0 7.2% 0 0;
  }
  .press__logos--solvable { width: 17.88%; }
  .press__logos--nc { width: 8.65%; }
  .press__logos--waratah { width: 32.78%; }
  .press__logos--bevel
  {
    width: 18.84%;
    margin: 0;
  }
}
```