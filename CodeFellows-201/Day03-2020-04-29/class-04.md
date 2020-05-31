# Read 04 - HTML Links, CSS Layouts, JS Functions

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 4 - Links

**Links** are the function of the world wide web that allow pages to be connected to each other.

A link can either be to another site entirely:

```HTML
<a href="https://www.bestsite.com">Link to Best Site Ever</a>
```

Or another page on the same site:

```HTML
<a href="generalinfo/aboutus.html">About Us</a>
```

Links can also employ id attributes in HTML to link to another part of the same page:

```HTML
<a href="#about-us-blurb">About Us Blurb</a>
```

Or a specific part of another page:

```HTML
<a href="https://www.bestsite.com/#best-part">Link to Best Site Ever</a>
```

## Chapter 15 - Layout

As discussed previously, CSS treats each HTML element as a box. How these boxes are laid out across a website determines a great deal of how the page looks, behaves, and how effectively it conveys the information it contains.

By default, browsers show pages in **normal flow** which stacks each **container element** vertically, creating a single column of elements. However there is also **relative positioning** (which moves one or more elements *relative* to where they would have been in normal flow), **absolute positioning** (which takes one or more elements out of their normal flow and causes the other elements to act as those the abosolute positioned ones aren't there), and **fixed positioning** (which I am struggling to differentiate from absolute positioning).

Elements can also be **floated** whereby the elements that follow will flow around them.

When designing the layout of a website, it is vital to take into consideration the variety of screen sizes in use today, from smart phones to 30 inch or larger monitors. A well designed website will look good at all these sizes.

There are pre-made **CSS frameworks** which are plug-and-play, in that you need to specify classes to your HTML elements so that they can be formatted by the framework.


## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 3 - Functions, Methods and Objects
## Pages 86 - 99

A **function** is a way of grouping code into a discrete unit which can be thought of as a machine that performs a particular task and produces a specific output.

In JS function looks like this:

```javascript
function getArea(x, y) {
    var rectangleArea = x * y;
    return rectangleArea;
}
```
Which calculates the area of any rectangle with a defined length and width. This function is called `getArea`, and has two **parameters**, `x` and `y`. To **invoke** (aka **call**) the function from elsewhere, the code would look like:

```javascript
getArea(10, 5);
```

Which would invoke and execute the function using the **arguments** `10` and `5`, multiple those two together, and return a value of 50. However, since we are not storing the returned value in the expression, we cannot do anything with it.

A more useful invocation would be:

```javascript
var myRectangleArea = getArea(10, 5);
```

Which then stores that calculated value of 50 for use elsewhere.

The above examples are **function declarations** which define a function that needs to be called eleswhere in the code. There are also **function expressions** which is when a function is used instead of an expression:

```javascript
var area = function(x, y) {
    var rectangleArea = x * y;
    return rectangleArea;
};
```

Note that we have ommitted the name (although you can use a name for function expressions); a function without a name is an **anonymous function**.

Function expressions assign the function to the variable, so to call the above function we would use the following:

```javascript
var myRectangleArea = area(10, 5);
```

There are also immediately invoked functions (called an **iffee**) which are executed as soon the code reaches them, and cannot be called again:

```javascript
var myRectangleArea = (function(x, y) {
    var rectangleArea = x * y;
    return rectangleArea;
});
```

Note the enclosing parentheses around the function.

**Variable scope** is an important aspect of creating functions and coding in general. A rule of thumb is that a variable should have as small of scope as possible. It is both wasteful in terms of memory, and confusing for reading your code, to use a **global scope** variable when a **function-level scope** variable will do. Additionally, if an HTML page uses multiple JS files (not uncommon) and they both declare the same global variable, it will produce a naming collision.


## [Article - 6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

**Pair programming** is the practice of two people simultaneously working on a project at the same workstation. Generally one person is doing the actual mechanical coding, the **driver** and the other is the **navigator**, who watches everything the driver is doing, keeps in mind the bigger picture and aspects that may escape the driver in the nitty gritty of coding. The driver and navigator actively discuss and problem solve together.

Pair programming has the advantage of being more efficient, forcing progammers to really address whether they know a subject by speaking it aloud, and pooling the knowledge and skillset of the driver and navigator. As part of this, both programmers gain knowledge from each other, and the collaborative research they do.

It is also an excellent way to practice teamwork and social skills, which are important for both job interviews and succeeding in most software developer positions.