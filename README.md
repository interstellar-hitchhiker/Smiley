# Smiley-Acid-Face1

Smile 


Go to: https://editor.p5js.org/

Paste in the code

Play 

Code - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
let pulseTimer = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(255);
  
  // draw yellow circle
  fill(255, 255, 0);
  ellipse(width/2, height/2, 300, 300);
  
  // draw black eyes
  fill(0);
  noStroke();
  ellipse(width/2 - 60, height/2 - 40, 80, 120);
  ellipse(width/2 + 60, height/2 - 40, 80, 120);
  
  // draw white circles inside black eyes with pulsating size
  fill(255);
  
  let size = map(sin(pulseTimer), -1, 1, 20, 55);
  
  ellipse(width/2 - 50, height/2 - 30, size, size);
  ellipse(width/2 + 50, height/2 - 30, size, size);
  
  // draw smiling mouth
  stroke(0);
  strokeWeight(5);
  noFill();
  arc(width/2, height/2 + 60, 120, 80, 0, PI);
  
  // increment pulse timer
  pulseTimer = (pulseTimer + 0.05) % TWO_PI;
}
