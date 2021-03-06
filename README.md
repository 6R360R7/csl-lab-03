# CSL Lab 03 - Variables

## How can I create custom variables to hold values in my p5.js projects?

# Overview
In this learning activity, students create their own variables to set the position, size and grey scale color of their shapes without repeating code.

# Objectives

## Students will be able to:
* Identify repeated values in their code and use variables in their place.
* Create and implement custom variables

# Vocabulary
| **Variables** | In CS, variables hold an assigned value or data of a specific type, they can also hold arrays of values which will be introduced later. | 
| --- | --- |
| **Width** | System variable that holds width of canvas as declared in set up. | 
| **Height** | System variable that holds height of canvas as declared in setup. | 
| **MouseX** | System variable that holds the current x-position of the mouse. | 
| **MouseY** | System variable that holds the current y-position of the mouse. | 
| **`console.log()`** | A function that logs a value to the console when the program is run. | 

# Resources
* [Ellipse Variable Intro](http://alpha.editor.p5js.org/cs4all/sketches/rJsRRER7Q)
* [Code Along 2 (with original code)](http://alpha.editor.p5js.org/cs4all/sketches/H1zfOrRXX)
* Video Tutorial: [2.2 Variables in p5.js (make your own)](https://www.youtube.com/watch?v=Bn_B3T_Vbxs&index=6&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA) | [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js/2.2_Variables_in_p5.js_user_defined)
* [2.1 Variables in p5.js](https://www.youtube.com/watch?v=diGjw5tghYU)
* [2.2 Variables in p5.js (Make your own)](https://youtu.be/Bn_B3T_Vbxs)

# Instructions

## Center elements with built-in variables: width and height
We have already used two built-in variables in the previous learning activity: mouseX and mouseY. Variables are placeholder names for values that change over time. We type mouseX knowing that p5 will replace that name with a number that represents the latest X position of the mouse. This number will change as the user moves the mouse across the canvas.
Next we will use two other variables built into p5: width and height. In the following example, their values are 600 and 240 ––the dimensions we gave our canvas when we created it in the setup function.

```javascript
function setup() {
 createCanvas(600, 240);

}

function draw() {
	background(180);

	//Draw the value of the width variable on the screen
	text(width, 40, 40);

	//Draw the value of the height variable on the screen
	text(height, 40, 60);

}

```

In the sketch below we use `width` and `height` to place an ellipse at the center of the screen:

```javascript
function setup() {
 createCanvas(600, 240);
}

function draw() {
	background(180);
 	ellipse(width/2, height/2, 60, 60);
}
```

The advantage of using these variables to place our ellipse is that, if we change the size of our sketch later, the ellipse will still be centered. To prove this, try changing the width and height of the canvas to 500 and 200, and run the sketch again.

width and height can also be used to place shapes in positions like "a third of the screen across", or "two thirds of the screen across", or "two thirds of the screen down". Try drawing these:

* `ellipse(width/3, height/2, 60, 60);`
* `ellipse(2*width/3, height/2, 60, 60);`
* `ellipse(width/3, 2*height/3, 60, 60);`
