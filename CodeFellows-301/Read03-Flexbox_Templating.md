# Read 03 - Flexbox and Templating

## [Javascript Templating Language and Engine— Mustache.js with Node and Express](https://medium.com/@1sherlynn/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)

There honestly wasn't a lot here. I feel like we'll dive into this more tomorrow, but basically all I saw here was that **mustache.js** allows you to have pass a JSON object into a mustache.js method along with a string that also contains `{{keys}}` with corresponding values in the JSON object, and mustache.js renders the appropriate values.

This article isn't ver clear how this allows for "templating" (unless one is already familiar with mustache?). I did some additional digging online and found a few examples that shed more light on it, but really I'm just going to wait to actually use this.

## [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

I've honestly already seen this article multiple times, and used it. I used it for Lab 01. The **flexbox** is a CSS layout that allows us to turn a container element into a flexible grid whose children elements flow and fall within that grid in a variety of specified ways.

We designate a flexbox as follows:

```CSS
.container-element {
  display: flex;
}
```

We can specify such additional properities as whether the elements within the flexbox will be rows or columns, and whether those rows or columns will flow from left-to-right (the default), top-to-bottom, or the opposite.

```CSS
.container-element {
  display: flex;
  flex-direction: column-reverse;
}
```

Flexboxes also allow us to easily center elements within the container element:

```CSS
.container-element {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

(Although to be fair that works great for one element, not so sure about multiple yet.)

Flexboxes are great, and in my limited experience, make RWD much easier. 