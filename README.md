![](headers/head2.2.jpg)
# Introduction to HTML5 elements and meta tags

Let's have a look at our initial markup.

We're going to use the **HTML5 doctype** as it's simpler to write, and it allows us to use the new HTML5 structural elements. This doctype will also trigger the validation of the document based on the HTML5 specifications.

```html
<!doctype html>
```

The **language** of the document should be defined in the `html` element. A value of `en` (English) will be used.

```html
<html lang="en">
```

All HTML documents should include **character encoding**. Charset should reside before the `title` element:

```html
<meta charset="utf-8">
```

Internet Explorer 8/9/10 support **document compatibility** modes which affect the way web pages are interpreted and displayed. Even if your site's visitors are using a modern version of Internet Explorer, their browser may not be using the latest rendering engine. So by specifying:

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

we are forcing Internet Explorer 8/9/10 to render the web page in the highest available document mode.

The `viewport` meta tag allows web developers to control the viewport's **size** and **scale**. A wide range of other mobile devices support this element. By default, most websites are scaled down to fit the size of the mobile screen, and the `viewport` meta element allows developers to determine the **width**, **height**, **initial scale**, **minimum scale** and **maximum scale** of the page. Ideally, the initial scale should be set to `1` so the layout will be viewed as intended in all devices. 

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

The minimum scale and maximum scale should be avoided as these values can present accessibility issues for some users: they won't be able to re-scale the layout to suit their needs.

# Adding HTML meta tags to support social networking sites

**Google Authorship and Publisher Markup** can be added to your HTML document. This will allow you to add links to your Google+ page in search results.

```html
<meta itemprop="name" content="correlate - A smarter expense tracker">
<meta itemprop="description" content="correlate is an easy to use, smarter expense tracker">
<meta itemprop="image" content="http://correlate.com/correlate.png">
```

**Twitter information** can be added to control how the website appears when shared via Twitter.

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@correlate-news">
<meta name="twitter:title" content="correlate - A smarter expense tracker">
<meta name="twitter:description" content="correlate is an easy to use, smarter expense tracker">
<meta name="twitter:creator" content="@author_handle">
<meta name="twitter:image:src" content="http://correlate.com/correlate.png">
```

You can employ things like Twitter card, Twitter site, Twitter title, Twitter description, Twitter creator, and even Twitter image.

**Open Graph** information can be added to control how your web page is displayed when shared on Facebook. First of all, you need to add a prefix into the `html` element:

```html
<html prefix="og: http://ogp.me/ns#" lang="en">
```

And then you can put a whole range of meta elements including open graph title, open graph type, url image and description:

```html
<meta property="og:title" content="Correlate">
<meta property="og:type" content="website">
<meta property="og:url" content="http://correlate.com">
<meta property="og:image" content="http://correlate.com/correlate.png">
<meta property="og:description" content="correlate is an easy to use, smarter expense tracker">
```


# Working with Apple touch icons

**Apple touch icons** are files that are displayed as icons on various Apple devices. For example, when someone bookmarks your web page or adds your web page to their home screen on a mobile device, one of these icons will be used. Apple touch icons are also supported by a variety of other devices including Android and Blackberry. You can create just a single Apple touch icon and then link to this icon from within your HTML file. However, if you want more control, you can create a unique Apple touch icon for all the possible size combinations and then link to all of them from within your HTML file. In the HTML file these links should be written from the largest size to the smallest one with the default touch icon written last as it will be used as a fallback.

```html
<link rel="icon" sizes="192x192" href="touch-icon-192x192.png">
<link rel="apple-touch-icon-precomposed" sizes="180x180" href="apple-touch-icon-180x180-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="152x152" href="apple-touch-icon-152x152-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="144x144" href="apple-touch-icon-144x144-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="120x120" href="apple-touch-icon-120x120-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="114x114" href="apple-touch-icon-114x114-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="76x76" href="apple-touch-icon-76x76-precomposed.png">
<link rel="apple-touch-icon-precomposed" sizes="72x72" href="apple-touch-icon-72x72-precomposed.png">
<link rel="apple-touch-icon-precomposed" href="apple-touch-icon-precomposed.png">
```

# Working with Favicons

A **favicon**, or a **favorites icon** is a file containing one or more small icons associated with a particular web site. You may see those icons up in the tab, in the address bar, in your bookmarks, in your history and on your welcome screen for Windows 8. Favicons generally include a range of different sizes, but they're all stored in a single file with an *.ico* extension. Like Apple touch icons, there are a range of different size: 120, 64, 48, 32, 24, and the default 16. Many online tools and applications exist that can help compiling *.ico* files. I use Icon Slate, but there are definitely a wide range of others out there as well.

```html
<link rel="shortcut icon" href="/favicon.ico">
```

# Working with MS icons

**MS icons** are used as icons for the various Windows devices. And there are a wide range of them including setting up an initial tile color. You can set up particular sizes for 144x144, 310x310, 310x150, 150x150, and 70x70.

```html
<meta name="msapplication-TileColor" content="#FFFFFF">
<meta name="msapplication-TileImage" content="assets/img/ms-icon-144x144.png">
<meta name="msapplication-square310x310logo" content="assets/img/ms-icon-310x310.png">
<meta name="msapplication-wide310x150logo" content="assets/img/ms-icon-310x150.png">
<meta name="msapplication-square150x150logo" content="assets/img/ms-icon-150x150.png">
<meta name="msapplication-square70x70logo" content="assets/img/ms-icon-70x70.png">
```

# Introduction to conditional comments for IE

When we talked about folders, I've mentioned two different *.js* files: *html5.js* and *respond.min.js*. If you look at the markup, you'll see that both of these are wrapped inside a **conditional comment**. Condition comments are the conditional statements interpreted by Internet Explorer that are used to provide or hide code for different version of Internet Explorer. In our case we are using `lt IE 9` which stands for **less than IE 9**.

```html
<!--[if lt IE 9]>
	<script src="assets/js/html5.js"></script>
	<script src="assets/js/respond.min.js"></script>
<![endif]-->
```

# Introduction to WAI-ARIA

**WAI-ARIA (Accessible Rich Internet Applications)** allows to describe elements and page modules using **properties**, **states** and **roles**. This makes widgets and dynamic content more accessible. Landmark roles help us to describe the overall document structure to assist devices such as screen readers. Landmark roles are well supported by JAWS, NVDA, and Voiceover. These roles are announced to the screen reader or braille device like navigation landmark. Users can use keyboard shortcuts or dialog boxes to navigate around web pages via these landmark roles. We are going to use the following ones:

```html
<header role="banner"></header>

<nav role="navigation"></nav>

<footer role="contentinfo"></footer>
```