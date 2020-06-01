# Read 01 - SMACSS and Responsive Web Design

## [Shay Howe's Intro to RWD](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

**Responsive web design** (RWD) is the practice of designing websites that dynamically adapt to the myriad of screen sizes used on internet connected devices.

Other approaches to various screen sizes are **Adaptive** and **Mobile** web design. Adaptive generally refers to having a set of built-in defaults in a website's layout, such that the site can adapt based off where a screen size falls within those defaults. Mobile is generally a separate site built for mobile devices. However, RWD is generally the preferred approach, as it is more flexible, and offers better maintainability.

Honestly, beyond that, this article didn't really make much sense to me. Despite looking up other sources, I still don't understand how all the pieces mentioned here fit into a whole website.

I think this is something that will have to wait for me to use it, and/or be less sleep deprived from working on my professional pitch.

## [All About Floats](https://css-tricks.com/all-about-floats/)

**Float** is a CSS property that allows us keep an element part of the normal flow of a website, but shift it to the left or right hand side of the page with other elements flowing around it. `float: left;` and `float: right;` float the element they are applied to to the left or right side of the page, respectively. `float: none;` (the default) tells an element to not float. `float: inherit;` causes an element to inherit its parent's float.

One thing this article did clear up which I have run into before: why a parent element all of whose children are floated collapses to zero height. The solution of clearing the float before the end of the container makes sense.