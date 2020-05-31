# Read 05 - HTML Images, CSS Color and Text

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 5 - Images:

Images are added to websites generally through HTML, via the `<img>` tag. Each `<img>` tag requires an `src` attribute, which tells the browser where to find the image. The `src` can be online or local on the machine serving the website:

```HTML
<img src="https://www.stockimages.com/beavers/beaver05728-GB.jpg" alt="brown-beaver" title="A brown beaver of Canada."/>
```

```HTML
<img src="images/beaver05728-GB.jpg" alt="brown-beaver" title="A brown beaver of Canada."/>
```

Note we also used the `alt` and `title` attributes. `alt` is a description of the image which is often important for screen reading software. `title` is desplayed by most browsers when the mouse cursor hovers over an image.

When creating/formatting/saving images for use on websites, it is best to match the actual size the image, in pixels, the image will be displayed in. 

HTML5 added the `<figure>` and `<figcaption>` tags:

```HTML
<figure>
  <img src="images/beaver05728-GB.jpg" alt="brown-beaver" title="A brown beaver of Canada."/>
  <figcaption>A brown beaver of Canada.</figcaption>
</figure>
```

That allows an image and its caption to be connected. A single caption can be associated with multiple images in this way.


## Chapter 11 - Color:

CSS can be used to assign color to HTML elements using color names (like `blue` or `orange`), or RGB, hex code values. CSS3 added RGBA (RGB with an alpha property, for transparency), HSL (hue saturation and lightness), and HSLA (HSL with an alpha property).

Color is one of the fundamental ways of making a website more attractive, readable, and make sure the information you want conveyed is easy to grasp.


## Chapter 12 - Text:

CSS is employed to modify how HTML text displays in web browsers. This is done through a number of properties that modify the text's weight, style, size, spacing, and font.

The font used to display text is set using the `font-family` property:

```CSS
font-family: Georgia, serif;
```

Note that the above property has two separate font values: "Georgia", and "serif". This allows the `font-family` property to use descending priority values, from left to right, so that if a preferred font is not available on the computer rendering a website, a backup font, or font type, can be used. In the above case, we are asking the browser to use the Georgia font, if available, and if not, use the default serif font. Any number of fonts and font types can be designated in this way:

```CSS
font-family: "Times New Roman", Times, serif;
```

 Additionally, there are **psuedo-elements** that allow selectors like `:first-letter`, and **psuedo-classes** that allow aspects of HTML text to be selected, like `:hover` and `:visited`