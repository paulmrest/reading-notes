# Read 07 - HTML Tables, and JS Constructor Functions

## [Summary of Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

One of the powers of **object oriented programming** (OOP) is that conceptual models in code can be transformed into reusable templates:

```JavaScript
var Cup = function(capacityOunces, heightInches, hasHandle) {
  this.capacityOunces = capacityOunces;
  this.heightInches = heightInches;
  this.hasHandle = hasHandle;
}

var tallNarrowCup = new Cup(12, 12, false);
var shortWideCup = new Cup(16, 6, true);
```

In the above example we have created a **constructor** function that creates an object. We then invoke that function with the **new** keyword, thereby creating a new object which is assigned to the designated variable.

An object has both **states** and **behaviors**. In the above example, we are only using states (properties), but an object can also have **methods** (functions internal to an object) which can be invoked on instances of the object.

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 6 - Tables

Tables in HTML offer the abilty to display data in a grid format.

The basic structure of a table (with headers) in HTML is:

```HTML
<table>
  <tr>
    <th></th>
    <th scope="col">Column Header 1</th>
    <th scope="col">Column Header 2</th>
  </tr>
  <tr>
    <th scope="row">Row Header 1</th>
    <td>Column 1, Row 1</td>
    <td>Column 2, Row 1</td>
  </tr>
  <tr>
    <th scope="row">Row Header 2</th>
    <td>Column 1, Row 2</td>
    <td>Column 2, Row 2</td>
  </tr>
</table>
```

## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 3 - Functions, Methods, and Objects
## Page 106 - 144

As it is late, my brain is rapidly turning to mush, and I am already familiar with OOP, I am going to just write up a quick thing on the one thing that really stood out to me here.

You can *add* and *delete* properities to JS objects. This just kind of blows my mind in how I think about OOP. Sure, objects can be mutable, but not *that* mutable.

Is this also the case for objects defined by class declarations, or just object literals? What was the original function of this capacity? I've done a little digging online, but haven't found anything satisfactory yet.

I'm looking forward to getting deeper into JS's approach to OOP.