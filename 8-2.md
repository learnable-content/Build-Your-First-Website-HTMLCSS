![](headers/head8.2.jpg)

# Planning and creating HTML elements for footer area

Paste the following code into *index.html*:

```html
<div class="row row--dark-grey row--padding-medium footer">
  <footer class="row container-wide" role="contentinfo">
    <div class="col-wide footer__info">
      <div class="footer__logo">
        <img src="assets/img/logo-correlate.png" alt="correlate">
      </div>
      <div class="row">
        <div class="col-medium">
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">FAQ</a></li>
          </ul>
        </div>
        <div class="col-medium">
          <ul>
            <li><a href="#">Facebook</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">Google+</a></li>
          </ul>
        </div>
      </div>
      <div class="row footer__copyright">
        <ul>
          <li>&copy; 2014 Correlate INC.</li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Terms</a></li>
        </ul>
      </div>
    </div>
    <div class="col-narrow--right footer__cta">
      <a href="#"><img src="assets/img/icon-cta.png" alt="App store"></a>
    </div>
  </footer>
</div>
```

# Styling footer area

Now paste styles for footer into *modules.css*:

```css
.footer__info { color: #777; }
.footer__info ul
{
  margin: 0;
  padding: 0;
  list-style: none;
}
.footer__info a:link,
.footer__info a:visited
{
  color: #777;
  text-decoration: none;
}
.footer__info a:focus,
.footer__info a:hover,
.footer__info a:active { border-bottom: .15em solid; }
.footer__info a:focus { color: #fff; }
.footer__info a:hover { color: #3bb2d0; }
.footer__info a:active { color: #56b880; }
.footer__logo { margin: 0 0 2em; }
.footer__copyright { margin: 1em 0 0; }
.footer__copyright li
{
  display: inline-block;
  margin: 0 1em 0 0;
}
```

# Creating footer styles for wide screens:

And lastly styles for wide screens:

```css
@media (min-width: 38em)
{
	.footer__cta { text-align: right; }
}
```

Go on and check how this looks in the browser.