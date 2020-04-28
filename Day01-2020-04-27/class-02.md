# Read 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 2 - Text:

Most websites primarily employ text for content. The different purposes that text serves in communicating on sites (header, body, paragraphs) can be delineated on a website using **markup tags** (such as `<h1>`, `<body>`, and `<p>`).

Tags are generally opened (`<h1>`), and closed (`</h1>`):

```HTML
<h1>This is header text that will show on the website</h1>
```
The above tags are all examples of **structural tags**, which generally describe the *kind* of text in the tags. Structural tags can either be **block** or **inline** tags (also called block or inline **elements**). A block tag/element starts a new line. Examples of block tags are `<p>`, `<div>`, and `<h1>`. Inline tags provide a way of delineating a chunk of text without creating a new line. Examples of inline tags are `<span>` and `<a>`.

In addition to structural tags, there are also **semantic tags** which provide additional information without necessarily being structural. Examples of this are <strong> and <em> (emphasis):

```HTML
<p>Here is a paragraph and one <em>emphasized</em> word.</p>
```

## Chapter 10 - Introducing CSS:

**CSS** (cascading style sheets) is a formatting language that allows websites to have more elaborate and interesting appearances than is possible with straight HTML. CSS treats each HTML as a box, with styling applied to different parts of that box (background, text, etc..). One uses **selectors** to designate which HTML elements are styled by which **declarations**. Declarations in turn are composed of **properties** (which designate which property of the HTML element is being styled, for example we might specify both the font family and the font color in the same declaration, but using two different properites), and values, which are what is assigned to a given property.

CSS is generally written in a separate document called a **style sheet**, but it can be added to an HTML document directly. The latter is generally only advisable for single page websites, as otherwise the same CSS would need to be added to multiple documents.

The *cascading* part of CSS refers to the fact that the value cascades, with later assignments superseding early ones (with some exceptions). So if an HTML element is given a color assignment at the beginning of a CSS sheet, and then that same HTML element is given a different color at the end, the last color will supersede the first.


## Summaries of John Duckett's Book, "JavaScript & JQuery":

## Chapter 2 - Basic JavaScript Instructions

JavaScript's (JS) construction includes **expressions** and **operators**.

Expressions are a statement that evaluates to a single value. An expression might look like:

`var foo = 10;`
or
`var bar = 5 + 5;`

Both of which evaluate to the same value, the number 10, but the latter evaluates the mathematical expression "5 + 5" first, and then completes expression.

Expressions such as the two above use the **assignment operator** ("=") to assign whatever is on its right side (the number 10 in the above examples) to a variable. In the above examples, `var` tells JS that the word that follows will be a variable, and the word is the name of the variable, `foo` and `bar` above, respectively.

There are other **operators** besides the assignment operator. **Arithmatic operators** (`+`, `-`, `*`, `/`, etc.), **comparison operators** (`==`, `>`, `<=`, etc.), **logical operators** (`||`, `&&`, etc.), and a single **string operator** (`+`, which combines, or **concatinates** strings).


## Chapter 4 - Decisions & Loops

As a computer program progresses, it needs to be able to decide on which code path to take based off prior user inputs and/or program states. A game that had only one possible sequence of events would be boring indeed! These decisions are frequently accomplished via **if** and **if/else** statements.

 If/else statements require **comparison operators** like `==` (is equal to), `>=` (greater than or equal to), or `!=` (is not equal to) so that the code can compare values and determine what step to take next. For example, if a function returns the size of a room, comparison operators would be used to determine whether a given table would comfortably fit in that room, as in the below example.

```javascript
function buyTable(roomArea) {
    if (roomArea >= 300) //square feet
    {
      return true;
    }
    else
    {
      return false;
    }
}
```

Another important part of if/else is **logical operators** which are used to combine comparison operators into more complex statements. There are three main logical operators:
* && - logical and - returns true if, and only if, the expressions on *both* sides return true
* || - logical or - returns true if *either* expression on either side return true
* ! - logical not - inverts whatever expression it is applied to
Expanding on the above example:

```javascript
function buyTable(roomArea, moneyForTable) {
    if (roomArea >= 300 && moneyForTable) //square feet
    {
      return true;
    } 
    else
    {
      return false;
    }
}}
```

Alternatively:

```javascript
function buyTable(roomArea, moneyForTable) {
    if (roomArea < 300 || !moneyForTable) //square feet
    {
      return false;
    }
    else
    {
      return true;
    }
}
```

We can check for multiple logical conditions:

```javascript
function buyTable(roomArea, moneyForTable) {
    if (roomArea > 1500 && moneyForTable)
    {
      console.log('Why are you looking at table this cheap with that kind of room?');
    }
    else if (roomArea >= 300 && moneyForTable) //square feet
    {
      return true;
    } 
    else
    {
      return false;
    }
}}
```

Note that we put the check for `roomArea > 1500` *before* the check for `roomArea >= 300`. This is because every room that is > 1500 is also >= 300, so if we had the check for >= 300 first, the code would never be able to enter the path under that if statement.


# Git Commit Messages

## Summaries from [Chris Beam's "How to Write Git Commit Messages"](https://chris.beams.io/posts/git-commit/)

As a git project can have hundreds, thousands, or more, commit statements across multiple branches, it is vital that git commit statements be clear and descriptive.

Clear formatting using word wraps at 72 characters, line breaks, and subject lines that are limited to 50 characters and have the first word capitalized, among other rules, allow better readability.

Equally important is the voice in which git commit statements are written. Imperative mood allows the statement to be a command or a request, giving more clarity around *what* was changed, and *why* those changes were made.