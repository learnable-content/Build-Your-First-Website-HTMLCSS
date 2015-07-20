![](headers/head2.3.jpg)
# Introduction to image types in websites

At this step we are going to talk about the images. When planning a site build, we need to decide whether images should be **inline** - defined in HTML markup, - or **background** - defined in the CSS code.

Inline images are normally content-related, so that they add additional meaning to the surrounding content. Background images, on the other hand, are normally used for decoration. These images add to the overall design but are not as important to the content.

# Working with inline images

In the header area there's a logo called correlate, and also an Apple Store icon. I've decided these two would be best done as inline images.

Down below we have two large images which I think should be both inline. There is also a little avatar icon, which again could be an inline image.

Next there are four logos and another Apple Store icon. Theoretically the logos could be a sprite, which we'll talk about soon, but in this case, I thought inline images would be better.

# Working with background images

Banner is most often used as a background image, because we're going to swap it out, and change it at smallest grain. Background images will also be employed for things like our bicycle, our phone, and save etc. These could be inline images but I felt that they were much more decoration than content-related so they're more background images.

And then we have four little background images for the icons. This brings up the subject of **sprites**.

# Working with sprites

An image sprite is a collection of images placed into a single image. A web page may have many images, and fetching each image generates a server request. Images using sprites allows us to reduce the number of server requests, which in turn decreases load time and improves the performance of the website.

While you could use powerful image editing tools like Photoshop, Fireworks, Illustrator or Sketch, you can also employ one of the many free online image sprite generators. Some examples include Sprite Cow, CSS sprite Generator, and SpritePad.