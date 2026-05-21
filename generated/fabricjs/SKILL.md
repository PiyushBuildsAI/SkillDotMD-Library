---
name: fabricJs
description: Use this skill when working with Fabric.js. Triggers when user mentions Fabric.js or imports from it.
---

# Fabric.js

## What this is
Fabric.js is a powerful and lightweight JavaScript library for working with 2D objects in HTML5 canvas elements. It provides an extensive set of tools for creating, manipulating, and interacting with objects on the canvas. With Fabric.js, you can create complex graphics, animations, and interactive applications.

## Installation
```bash
npm install fabric
```

## Key concepts
Fabric.js provides several key concepts, including:
* **Canvas**: The main element that renders the 2D objects. Created using `new fabric.Canvas('canvas')`.
* **Objects**: The 2D elements that can be added to the canvas, such as rectangles, circles, and text. Created using `new fabric.Rect()`, `new fabric.Circle()`, etc.
* **Event handling**: Fabric.js provides various events, such as `object:moved`, `object:modified`, and `mouse:down`, that can be used to interact with the objects on the canvas.

## Correct usage patterns
Here's an example of creating a canvas and adding a rectangle to it:
```javascript
var canvas = new fabric.Canvas('canvas');
var rect = new fabric.Rect({
  left: 100,
  top: 100,
  fill: 'red',
  width: 200,
  height: 200
});
canvas.add(rect);
```
And here's an example of handling an event:
```javascript
canvas.on('object:moved', function(options) {
  console.log(options.target);
});
```

## Common mistakes to avoid
Common mistakes include:
* Forgetting to add objects to the canvas using `canvas.add()`.
* Not handling events properly, leading to unexpected behavior.
* Not using the correct options when creating objects, resulting in incorrect rendering.

## File and folder conventions
Fabric.js files are typically included in the HTML file using a script tag:
```html
<script src="https://cdn.jsdelivr.net/npm/fabric@4.6.0/dist/fabric.min.js"></script>
```
Canvas elements are usually placed in the HTML file:
```html
<canvas id="canvas" width="800" height="600"></canvas>
```
It's a good practice to keep the JavaScript code that interacts with the canvas in a separate file, and include it in the HTML file using a script tag.