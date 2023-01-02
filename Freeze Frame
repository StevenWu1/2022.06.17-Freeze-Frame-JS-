// The timestamp of your freeze frame
// TODO: Replace these zero values
let minutes = 4;
let seconds = 2;
let img;
// Screenshot of your freeze frame


// Canvas size; canvasHeight will be set during setup()
let canvasWidth = 400;
let canvasHeight;

// Adjust transparency level (between 0.0 and 1.0)
// while you work; then set to 1.0 for submission
let transparency = 1;

function preload() {
  // preload() runs once
  img = loadImage('FreezeFrame.PNG');
}
  // "Upload file" from the left sidebar, then load it here
  // TODO: Uncomment the next line, using appropriate filename
  // img = loadImage("YOUR-SCREENSHOT.{png|jpg|...}");

function setup() {
  if (img === undefined) {
    createCanvas(canvasWidth, );
    textSize(32);
    text("Upload file. Edit preload().", 10, 30);

  } else {

    // Rescale the image to 400px wide; canvasHeight will
    // be scaled proportionally. Set canvas size to that
    // of rescaled image. (don't modify next three lines)
    img.resize(canvasWidth*16/9, 400);
    canvasHeight = img.height;
    createCanvas(canvasWidth*16/9, canvasHeight);

    // TODO: If you need more setup(), do so here
  }
}

function draw() {
  drawOriginalImage();
  drawTransparentLayer();
  drawMyFreezeFrame();
  if (mouseIsPressed){
    console.log(mouseX, mouseY);
  }
}

function drawOriginalImage() {
  if (img !== undefined) {
    image(img, 0, 0);
  }
}

function drawTransparentLayer() {
  if (img !== undefined) {
    fill(255, 255, 255, transparency * 255);
    noStroke();
    rect(0, 0, canvasWidth * 16/9, canvasHeight);
  }
}

// function mouseMoved() {
//   console.log("mouseX = " + mouseX, "mouseY = " + mouseY);
// }

function drawMyFreezeFrame() {
  fill(241, 221, 40);
  rect(0, 0, width, height);
  head();
  nose();
  ears();
  fill("black");
  circle(360, 386, 10);
  cheeks();
  fill(128, 181, 1);
  eyes();
}

function head(){
  fill(50, 140, 255);
  quad(66, 400, 122, 266, 272, 250, 330, 400);
  quad(442, 234, 590, 268, 598, 400, 413, 331);
  quad(303, 331, 330, 400, 598, 400, 413, 331);
}

function nose() {
  fill("pink");
  triangle(303, 331, 413, 331, 356, 360);
}

function ears() {
  fill(0, 163, 250);
  triangle(514, 115, 442, 234, 590, 268);
  triangle(195, 115, 122, 266, 272, 250);
  quad(272, 250, 442, 234, 413, 331, 303, 331);
  fill("rgba(225, 168, 178, 1)");
  triangle(201, 158, 232, 224, 219, 219);
  triangle(237, 241, 220, 220, 157, 246);
  triangle(201, 158, 157, 246, 220, 220);
  triangle(540, 224, 476, 210, 512, 154);
  quad(474, 229, 486, 210, 531, 222, 550, 252);
}

function eyes(){
  fill(128, 181, 1);
  ellipse(214, 329, 90, 74);
  ellipse(492, 328, 90, 74);
  triangle(186, 299, 156, 328, 182, 356);
  triangle(240, 298, 274, 330, 239, 361);
  triangle(463, 298, 432, 330, 469, 360);
  triangle(523, 301, 550, 326, 516, 359);
  fill("black");
  triangle(198, 294, 200, 338, 174, 309);
  quad(198, 294, 200, 338, 226, 311, 225, 292);
  triangle(198+275, 294, 200+275, 338, 174+275, 309);
  quad(198+275, 294, 200+275, 338, 226+275, 311, 225+275, 292);
}

function cheeks() {
  fill("hotpink");
  ellipse(252, 386, 68, 40);
  ellipse(457, 385, 68, 38);
}
