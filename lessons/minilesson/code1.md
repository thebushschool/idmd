## Dynamic Sticks Example Starter Code
### While reading this example remember the graphics canvas coordinates are defined as follows:

![alt text](canvas_coords.svg)

### Computer Graphics coordinate system and shapes that we will use

<img src="graphics_coords.svg" alt="Graphics Coordinate System" width="800"/>

### Copy & Paste all the lines of code in the box below into the editor you previously opened  

```javascript
// Dynamic Sticks
// Learn to code visually!
// Anything following "//" are help comments !!
// Modify lines with "***AND ALL CAPS LETTERS like this"

// Do not worry about breaking anything as you can come back to the original version of this code!!

let loc = 0;  // set up a variable pixel location

function setup() {  // this function is run once.   
    // canvas size in pixels
    // width is set to 600, and height to 200
    createCanvas(600, 200); 

    // set the background color
    background("pink");  
    
    // limit the number of frames per second
    frameRate(10);
    
    // draw smooth lines
    smooth();

    // 1. Say Hello!
    // ***UNCOMMENT LINE BELOW BY DELETING THE 2 SLASHES TO SAY HELLO!
    // HIT THE PLAY BUTTON IN YOUR EDITOR
    //sayHello();
} 

function draw() {  // this function is run repeatedly.  

  // 2. Draw some sticks
  // ***UNCOMMENT LINE BELOW BY DELETING THE 2 SLASHES TO SEE WHAT HAPPENS!
  //drawSticks1();

  // 3. Draw more sticks
  drawSticks2();   
  
  // Move location for next draw loop
  moveLoc();
}

function sayHello() {
    // ***SAY HELLO TO YOUR FRIENDS - MODIFY TEXT BELOW!! 
    // use input parameters: quoted text, x loc & y loc
    textSize(20);
    text("Hello friends!", 10, height/2);
}

function drawSticks1() {
  // set the thickness of the line. 
    strokeWeight(10);
  // set a random color for the line 
    stroke(randomColor());
    
    // draw the line using input parameters:
    // 2 pairs of points: x1, y1, x2, y2 
    line(loc, 0, width/2, height); 
}

function drawSticks2() {
  // ***CAN YOU DRAW ANOTHER SET OF LINES 
  // FROM BOTTOM TO TOP? OR FROM LEFT TO RIGHT ??
  // YOU WILL NEED COPY CONTENTS OF drawSticks1() FUNCTION 
  // BETWEEN OUTER BRACKETS BELOW AND MODIFY JUST 
  // THE "line" FUNCTION CALL BELOW!
  // HINT: x1, y1 need to be fixed & x2 is var, y2 is fixed
  // 

}

function moveLoc() {
    // move loc over by 40 pixels
    // reset to 0 if width of canvas is exceeded!
    if (loc < width) {
        loc = loc + 40;
    } else {
        loc = 0; 
    }
}

function randomColor() {
  // return an array of random RGBA values for color
  // random(255) gives a random number 0 to 255 for each color and alpha
  return [random(255), random(255), random(255), 255];
}
```