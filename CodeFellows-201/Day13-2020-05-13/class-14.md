# Read 14A - CSS Transforms, Transitions, and Animations

## [What Google Learned From Its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

I feel like we can summarize the whole article with the following: empathy and sympathy is more important than any type of intelligence or accomplishments.

See how I left the word "team" out of that statement? That's because that rule of thumb isn't just about putting together teams, but it certainly manifests there as well.

Of course in the hyper-individualistic tech world of the individualistic United States, that people need to feel cared for and safe in a group setting to perform well can be a bit surprising. Alas, we are social creatures before we are individuals.

## [CSS Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

CSS3 introduced **transforms**. These allow for CSS properities that can alter an HTML element's shape in both two and three-dimensional space.

The basic syntax is:

```CSS
div {
  -webkit-transform: scale(1.5);
  -moz-transform: scale(1.5);
  -o-transform: scale(1.5);
  transform: scale(1.5);
}
```

Where all four properities do the same thing, but provide support for different browsers. If a browser supports full CSS transforms, it only uses the `transform: scale(1.5)` property.

Two-dimensional transforms allow for scales (proportionally and not), translations, skewing, and can be combined.

Three-dimensional transforms allow for rotations, perspective shifts, and their own translations.

## [CSS Transitions & Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

Also included with CSS3 was the ability to perform **transitions** and **animations** on HTML elements. There can be combined with to transition and animate transforms.