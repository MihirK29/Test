/*
  Description: Processing Assignment One
 Author: Mihir Kachroo
 Date of last edit: November 14
 */


IntList squaresX;
IntList squaresY;

int x;
int y;

void settings() {
  size(600, 600);
}

void setup() {
  background(100);
  squaresX = new IntList();
  squaresY = new IntList();

  for(int i=0; i<5; i+=1){
    squaresX.append((int)random(50,550));
    squaresY.append((int)random(50,550));
}

  rectMode(CENTER);
}


void draw() {

  //background(invertColor(r,b,g));
  for(int i=0; i<squaresX.size(); i+=1){
    x=squaresX.get(i);
    y=squaresY.get(i);
    fill(squareColour(x,y));
    rect(x,y,80,80);
  }
}

color squareColour( int XPos, int YPos) {
  return color(mouseX-XPos, mouseY-YPos, 250);
}


