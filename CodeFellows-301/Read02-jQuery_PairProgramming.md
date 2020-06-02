# Read 02 - jQuery, Events, and The DOM - Pair Programming

## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 7 - jQuery

**jQuery** is a JS framework that facilities a much more efficient mode of interaction between JS and HTML. It does this by allowing CSS-style selectors in order to identify HTML elements.

So to add a new element using pure JS we might do something like:

```javascript
let pTextContext = '...';
let newPElement = document.createElement('p');
newPElement.setAttribute('class', 'regular-paragraph');
newPElement.textContent = pTextContent;
document.getElementByID('parent-div').appendChild(newPElement);
```
With jQuery we can simply do this:

```javascript
$('#parent-div').append(<p class="regular-paragraph">...</p>);
```

Or even modify multiple elements simultanously:

```javascript
$('.regular-paragraph').addClass('another-paragraph-class');
```

Like in regular JS, finding nodes in the DOM takes resources, so if we are going to be using the same node(s) multiple times we want to assign it/them to a variable for later use:

```javascript
let $regularPEls = $('.regular-paragraph');
```

jQuery also includes a `ready()` method that is called once the page is done rendering so the DOM tree is complete:

```javascript
$(document).ready(function(){
  $('#parent-div').append(<p class="regular-paragraph">...</p>);
});
```

The `css()` method gives a quick and efficient way of modifying CSS from JS:

```javascript
$(document).ready(function(){
  $('#parent-div').css({
    'background-color': 'rgb(158, 158, 158)',
    'color': '#fff'
  });
});
```

jQuery also offers a number of methods such as `hide()` and `slideUp()` that can be used to animate elements, including specifying the animation's duration and even a function that is called upon completion.

jQuery can be downloaded and included as a file with your website, or simply loaded from a CDN. If using a CDN, it is advisible to use a backup local file as well.

## [Article - 6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
## [Copied from my 201 write-up on this after reading the article again and finding nothing new to say.](CodeFellows-201/Day03-2020-04-29/class-04.md)

**Pair programming** is the practice of two people simultaneously working on a project at the same workstation. Generally one person is doing the actual mechanical coding, the **driver** and the other is the **navigator**, who watches everything the driver is doing, keeps in mind the bigger picture and aspects that may escape the driver in the nitty gritty of coding. The driver and navigator actively discuss and problem solve together.

Pair programming has the advantage of being more efficient, forcing progammers to really address whether they know a subject by speaking it aloud, and pooling the knowledge and skillset of the driver and navigator. As part of this, both programmers gain knowledge from each other, and the collaborative research they do.

It is also an excellent way to practice teamwork and social skills, which are important for both job interviews and succeeding in most software developer positions.