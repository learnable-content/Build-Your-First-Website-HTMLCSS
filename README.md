![](headers/head6.1.jpg)
# Planning content and styles for features area:

In this lesson we're going to style the features and photos modules. If you look at the finished layout, you'll see that the features module is composed of rows with a class of `row` and `features__row`. They are virtually the same as the basic row apart from having extra margin. Inside each row we have `features__heading` and `features__text`. There is also graphics in the features: bike, phone, and safe. We're going to style it for small screen first, so initially they're all going to sit one on top of each other.

# Creating HTML elements for features

Open up *index.html* and paste the following code:

```html
<div class="row row--white row--padding-wide features">
  <div class="row container-medium">
    <div class="row features__row">
      <div class="col-narrow--right features__bike">
      </div>
      <div class="col-wide">
        <h2 class="features__heading">
          Easy to use, money management.
        </h2>
        <p class="features__text">
          Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
        </p>
      </div>
    </div>
    <div class="row features__row">
      <div class="col-narrow features__phone">
      </div>
      <div class="col-wide--right features__padding">
        <h2 class="features__heading">
          Day to day breakdown.
        </h2>
        <p class="features__text">
          Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
        </p>
      </div>
    </div>
    <div class="row features__row">
      <div class="col-narrow--right features__safe">
      </div>
      <div class="col-wide">
        <h2 class="features__heading">
          Connect securely with your bank.
        </h2>
        <p class="features__text">
          Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.
        </p>
      </div>
    </div>
  </div>
</div>
```

# Styling feature areas

Open up *modules.css* and paste:

```css
.features { text-align: center; }
.features__row
{
  margin-bottom: 2.1875em;
  /* 35px/16px */
}
.features__heading
{
  margin: 0 0 .75em;
  /* 12px/16px */
  font-size: 1.125em;
  /* 18px/16px */
}
.features__text { margin: 0; }
.features__bike
{
  height: 90px;
  background: url(../img/icon-bike.png) no-repeat center;
  background-size: contain;
}
.features__phone
{
  height: 149px;
  background: url(../img/icon-phone.png) no-repeat center;
  background-size: contain;
}
.features__safe
{
  height: 80px;
  background: url(../img/icon-safe.png) no-repeat center;
  background-size: contain;
}
```

# Creating Feature styles for wide screens

We've done the narrow screen version, so it is time to add media query to apply styling for wide screens:

```css
@media (min-width: 38em)
{
  .features { text-align: left; }
  .features__row
  {
    margin-bottom: 4.1667em;
    /* 75px/18px */
  }
  .features__row:last-child { margin: 0; }
  .features__padding
  {
    padding-top: 4em;
    /* 72px/18px */
  }
  .features__heading
  {
    font-size: 1.5556em;
    /* 75px/18px */
    font-weight: normal;
  }
}

@media (min-width: 50em)
{
  .features__bike { height: 154px; }
  .features__phone { height: 296px; }
  .features__safe { height: 141px; }
}
```