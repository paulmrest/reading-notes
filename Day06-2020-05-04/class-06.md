# Read 06 - JS Object Literals, The DOM

## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 3: Functions Methods and Objects
## Page 100 - 105: Object Literals

**Objects** are one way a programming language can create models of real world entities. An object consists of **properties** and **methods**:

```JavaScript
var cup = {
  capacityOunces: 10,
  heightInches: 5,
  hasHandle: false;,
  color: 'green',
  material: 'ceramic',

  fill: function() {
    console.log('Filling cup...');
  },

  drink: function() {
    console.log('Drinking from cup...');
  }
};
```

In the above example we're creating an **object literal** and assigning it to the var `cup`. This object has five properties: `capacityOunces`, `heightInches`, `hasHandle`, `color`, and `material`. It has two methods, `fill()` and `drink()`.

We can access the data stored in an object via **dot notation** or **bracket notation** (shown respectively below):

```JavaScript
var cupColor = cup.color; //'green'
var cupCapacity = cup['capacityOunces']; //10
```

We can invoke the methods in an object also via dot and bracket notation:

```JavaScript
cup.fill(); //'Filling cup...'
cup['drink'](); //'Drinking from cup...'
```


## Chapter 5: Document Object Model

A **document object model** (DOM) is the representation that a web browser builds of a site from its HTML, and the **DOM tree** is the structure that model takes for a given site.

The DOM tree allows JS to access, parse, and update the HTML and CSS of a site, including modifying the content of an HTML element, inserting new elements, and modifying and creating new CSS selectors.

A DOM tree consists of four types of **nodes**:
* Document: this is the top level node that represents the highest level of the site. All other nodes are under the document node.
* Element: these are the structural tags of HTML like <div> and <p> and <header>.
* Attribute: these are the attributes that can be a part of the HTML elements like class="a-class-name".
* Text: these are the text content that can be part of a given HTML element.

JS can select a given node a number of ways, but a couple of common examples:

```JavaScript
var oneElement = document.getElementByID('an-ID-name'); //returns one node, if it exists
var multipleElements = document.getElementsByClassName('a-class-name'); //returns multiple nodes, if any exist
```

A method like `getElementsByClass()` that can return multiple node will return a **NodeList**. A NodeList is a collection of elements that must be iterated over to access individual elements:

```JavaScript
for (var i = 0; i < multipleElements.length; i++>)
{
  //do something with each element, or use additional conditionals to find the element(s)
}
```

Note that while a NodeList looks and behaves similarly to an array, it is not an JS array.

Once we have a variable pointing at an individual node, there a number of methods for altering it:

```JavaScript
oneElement.textContent = 'Some new text for the world to see.'; //replaces the node's text content
oneElement.innerHTML = '<a href="https://www.linkedylink.com">New Link</a>'; //replaces the node's HTML with new HTML
```

As it is possible to alter the HTML and CSS of a site from JS, it is important to keep in mind what parts of a site a user is potentially given access to. A common example of this would be using JS that allows a user to insert new HTML into a page to insert a `<script>` tag that directs data elsewhere.