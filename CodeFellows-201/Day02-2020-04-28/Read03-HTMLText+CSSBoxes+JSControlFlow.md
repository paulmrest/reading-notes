# Read 03 - HTML Lists, CSS Boxes, and JS Control Flow

## Summaries from Jon Duckett's book, "HTML & CSS":

## Chapter 3 - Lists

HTML offers three types of list for organizing content:

* **Unordered**: for items with no specific or inherent order, like a list of foods available to eat.
* **Ordered**: for items with some specific or inherent order, like a list of foods in a refridgerator based off their expiration dates.
* **Definition**: for items followed by their definitions. Definition lists are unordered.

Lists can also be inside another list.

## Chapter 13 - Boxes

CSS interprets each HTML element as a box. So the HTML

```HTML
<div>
</div>
```

Would be a single box, while

```HTML
<div>
  <p>
  </p>
</div>
```

Would be two boxes, the `<p>` box *inside* the `<div>` box.

Part of formatting a website with CSS is manipulating these boxes's size, position and appearance.

There a number of properties that control size, position, and appearance, so we'll just go through a few of each.

* Size

`height: 250px;`
This would set the element's box to a static height of 250px.

`max-height: 800px;`
This would set the element's box to a *maximum* height of 800px, although the element's height could be less than that depending on other factors.

* Position

`margin: 25px;`
This would set a margin of 25px all the way around the *outside* an element, such that the outside border of the box will be 25px away from all other elements (including the edge of the page).

`padding: 50px;`
This sets a padding *inside* the HTML element's box, such that any content within the box will be at least 50px from the box's edge.

* Appearance

`border: 8px solid green;`
Without specifying a border property, borders are transparent and 0px. This property changes the border to being 8px thick, and solid and green in appearance.

`text-align: center;`
This centers any *text* inside the HTML element's box. Note that content other than text needs to be centered with a different property.

## Summaries of John Duckett's Book, "Javascript & JQuery":

## Chapter 4 - Decisions and Loops (p. 162 - 182)

In addition to if statments, JavaScript also has **if..else** statements. An if...else statment has a logical condition on the first code path, but then if that condition isn't met, then the execution will fall into the **else** block:

```JavaScript
var plantNeedsWater = false;
if (plantNeedsWater)
{
  waterPlant();
}
else
{
  //do something else
}
```

A **switch statment** is another way of choosing a given code path based off a logical condition:

```JavaScript
var cupsOfWaterPlantNeeds = 4;
switch (cupsOfWaterPlantNeeds)
{
  case 1:
    //run loop once
    break;
  case 2:
    //run loop twice
    break;
  case 3:
    //run loop thrice
    break;
  case 4:
    //run loop four times
    break;
  default:
    //handle invalid/unknown value
    break;
}
```

So in the above example the code path in `case 4:` would be run. If our variable cupsOfWaterPlantNeeds was <= 0 or > 4, the switch statement would choose the `default:` path.

JavaScript tries to handle unexpected data type matchups, such as comparing a number to a string. This is called **type coercion** and can lead to unexpected results. For example:

`'6' == 6`

Would evaluate to TRUE as JS will, behind the scenes, see that the `'6'` string can be parsed to a integer value and do so for the comparison. To avoid this, strict equality operators can be used:

`'6' === 6`

Will evaluate to FALSE.

As JS is frequently interacting with HTML elements, it needs to check whether an element exists in the HTML:

```JavaScript
if (document.getElementByID('best-ID-ever'))
{
  //do something with element
}
else
{
  //create string to insert into HTML
}
```

Even though the string returned by getElementByID() is not a boolean value, it is **truthy** and will evaluate to true. **Falsy** values include things like `''` (empty strings) and `0` (the number zero).

Loops are fundamental to programming, allowing, among other things, iteration through data and waiting on a valid state. There are **for** loops, **while** and **do while** loops.

```javascript
console.log('We\'re going to count to 10!');
for (var i = 1; i <= 10; i++)
{
    console.log('Counting to 10, presently at: ' + i);
}
```

```javascript
console.log('We\'re going to count to 10!');
var count = 1;
while (count <= 10)
{
    console.log('Counting to 10, presently at: ' + count);
    count++;
}
```

Both of which would display the same output:

> We're going to count to 10!
> Counting to 10, presently at: 1
> Counting to 10, presently at: 2
> Counting to 10, presently at: 3
> Counting to 10, presently at: 4
> Counting to 10, presently at: 5
> Counting to 10, presently at: 6
> Counting to 10, presently at: 7
> Counting to 10, presently at: 8
> Counting to 10, presently at: 9
> Counting to 10, presently at: 10

The difference between a while and a do while loop is that the while loop checks the condition *before* entering the loop, while a do while loop does so *after*. So a while loop may never execute at all, while a do while loop always executes at least once.