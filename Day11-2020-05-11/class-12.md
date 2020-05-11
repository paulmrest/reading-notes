# Read 12 - Docs For the HTML `<canvas>` Element & Chart.js

## [Chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

Chart.js is a JS plugin that allows easy access to prettily rendered graphs and charts. The plugin draws inside of an HTML5 `<canvas>` element.

With a `<canvas>` element in place, we can create a line graph inside of it:

```JavaScript
var lineGraphCanvasEl = document.getElementById('canvas-id').getContext('2d');
new Chart(lineGraphCanvasEl).Line(lineGraphData);

var lineGraphData = {
  //line graph data, including labels and datasets
};
```
Note that the `GetContent('2d')` method invocation is getting the rendering context.

This then would daw the line graph in your `<canvas>` element.

## MDN <canvas> ELement Documentation
[Basic Usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)
[Drawing Shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
[Applying Styles](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)
[Drawing Text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

The HTML5 `<canvas>` element is used to create new renderings. It only has two attributes, `width` and `height`, then everything else is done in JS.

The first part of drawing in a `<canvas>` element is to get the rendering context:

```JavaScript
var canvasCtx = document.getElementByID('canvas-id').getContent('2d');
```

Note that the "2d" context is for rendering things in two-dimensions. `<canvas>` elements have other rendering contexts, like "WebGL" which is a varient of OpenGL.

Drawing can be done by calling methods to create specific shapes:

```JavaScript
var canvasCtx = document.getElementByID('canvas-id').getContent('2d');

canvasCtx.fillRect(30, 30, 150, 150);
```

The above code would draw a black rectange 150 by 150 pixels, with its origin (upper left) at x = 30 and y = 30. Note that we can draw in other colors as well:

```JavaScript
var canvasCtx = document.getElementByID('canvas-id').getContent('2d');

canvasCtx.fillStyle = 'rgb(255, 230, 0)';
canvasCtx.fillRect(30, 30, 150, 150);
```

Would draw the same rectange, only in yellow.

Drawing can also be done by specifying paths that follow arcs and lines:

```JavaScript
var canvasCtx = document.getElementByID('canvas-id').getContent('2d');

canvasCtx.fillStyle = 'rgb(255, 230, 0)';
canvasCtx.beginPath();
canvasCtx.moveTo(30, 30);
canvasCtx.lineTo(180, 30);
canvasCtx.lineTo(180, 180);
canvasCtx.lineTo(30, 180);
canvasCtx.fill();
```

Creates the same yellow square.

Drawing arcs can be done via the `arc()` method for simple curves, or via Bezier and quadratic curves for more complex ones.

Text can also be rendered in a `<canvas>` element:

```JavaScript
var canvasCtx = document.getElementByID('canvas-id').getContent('2d');

canvasCtx.font = '36pt serif';
canvasCtx.strokeText('Hello out there!', 30, 30);
```

Which would draw the string "Hello out there!" starting at x = 30 and y = 30.

Text, simple shapes, and more coplicated shapes can all be sytled a number of ways beyond the scope of these notes. See above links for more information.