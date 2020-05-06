# Read 09 - Forms and Events

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 7 - Forms

**Forms** in HTML offer a way of gathering information a site is asking from a user into a single unit. Elements within a form can include textboxes, radio buttons, checkboxes, drop down lists, and buttons. Information from form elements is sent to a server as **name/value** pairs.

```HTML
<form action="https//www.server.com/coolapp.php">
  <input type="text" name="username"/>
</form>
```

In the above example, we are putting a text box on the page, and when whatever a user has entered in the textbox is sent submitted, it is sent to https://www.server.com/coolapp.php with the name/value pair "username/USER ENTERED TEXT".

Form elements also allow for validation with attributes like `maxLength`.


## Chapter 14 - Lists, Tables, and Forms

CSS has a number of properties specifically for lists, tables, and forms.

Lists - without default browser formatting, an HTML list will display as just a column of text. `list-style-type` and `list-style` allow basic formatting of a list including the style of bullet point. `list-style-image` allows custom images to be used for bullet points.

Tables - similarly to lists, tables, without any formatting, display as a series of columns of text and are generally difficult to read. CSS allows borders to be displayed for each `th` and `td` element, margins and padding to be configured between the cells, header and body elements to be formatted differently from the body, and so on.

Forms - styled similarly to other HTML elements, the text labels on input elements can have properities applied to them to change the font, color, etc... Additionally, the text input boxes themselves can be formatted, with properities like `border-radius` used to create a text input box with rounded corners.


## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 6 - Events

Web browsers, like most computer software that users interact with, register a number of **events**. These include mouse clicks, mouse downs, key presses, page loads, window resizes, and even when changes are made to the DOM.

Part of an interactive site is the ability to catch and do something with those events. HTML the ability to catch events and send them to JS functions via **event handler** attributes, however this is an older method as having JS in your HTML is considered bad pratice.

The next way of handling events is **traditional DOM event handlers**:

```JavaScript
var anHTMLElement = document.getElementByID('HTML-elment-ID');
anHTMLElement.onclick = bestFunctionEver;
```

The above code binds the event handler `onclick` to the HTML element, and then when that event occurs (a mouse click) calls the function `bestFunctionEver()`.

The most recent way of handling events if **event listeners**:

```JavaScript
var anHTMLElement = document.getElementByID('HTML-elment-ID');
anHTMLElement.addEventListender('onclick', bestFunctionEver, false);
```

Note the third parameter, `event flow`. When set to `false`, the event flows from the most specific HTML element to the least specific. When set to `true`, this order is reversed. `false` is considered the default.

Events themselves are objects which contain a number of properities about the event's target, type, and others. An event can be captured thus:

```JavaScript
var anHTMLElement = document.getElementByID('HTML-elment-ID');
anHTMLElement.addEventListender('onclick', function(event) {
  bestFunctionEver(event);
}, false);

function bestFunctionEver(event) {
  var eventTarget = event.target;
  //best function stuff
}
```

Note that in order to set up an event listener to pass an argument to a function, an anonymous function must be used that calls the actual function.