![](headers/head9.1.jpg)
# Introduction to HTML and CSS validation

In this final lesson we are going to discuss validation and testing.

**Validation** is a process of checking documents to make sure that they comply with standards that have been set by the **W3C (World Wide Web Consortium)**.

* HTML files can be validated using the **W3C Markup Validation Service**.
* HTML5 files can also be validated using the **Nu Markup Checker**, which is an experimental checker.
* CSS files can be checked using the **W3C CSS Validation Service**.
* CSS files can also be checked using a range of other online services such as **CSS Lint**. This service checks not only for conformance, but also makes sure your CSS has been abstracted as much as possible.

# Understanding the importance of validation

Why should you validate your code? Validation is one of the simplest ways to check whether a page is built in accordance with Web standards. It provides one of the most reliable guarantees that future web platforms will handle your files as designed. Validating your markup and CSS allows you to check for and quickly resolve bugs.

# Validating HTML and CSS of index file

So, let's go and validate our HTML and CSS files. Open the following pages in your browser:

* [http://validator.w3.org](http://validator.w3.org/) - W3C Markup Validation Service.
* [http://jigsaw.w3.org/css-validator](http://jigsaw.w3.org/css-validator) - W3C CSS Validation Service.
* [http://csslint.net](http://csslint.net) - CSS Lint tool.

Start with the HTML validation service first. All we need to do is switch to Validate by File Upload tab and choose *index.html* file.

You will see three errors on line 10, 11, and 12. These lines have meta information for Google and if you feel that these are going to cause more problems then their benefits, you can just delete these lines.

Now let's validate our CSS files. Open By file upload tab and check *.css* files individually. You should see that all those files are valid.

Now let's have a look at our last tool called CSS Lint. For this one it's actually best if all your CSS is uploaded together. So you may copy contents from the *base.css*, *layout.css* and *module.css* into one file and paste the result into the text area.

There should be no errors and one warning saying there are too many `font-size` declarations. There's actually 19 of them, and some abstraction is needed. On a small site like our demo, that's not too much of a problem, but if you're working on a large site, it is probably a good idea to abstract your font sizes. Instead of declaring them multiple times, you'd create specific classes like we did for rows and create a set of fonts that can be applied as needed. That way, your CSS files would become much more tidy and lean.