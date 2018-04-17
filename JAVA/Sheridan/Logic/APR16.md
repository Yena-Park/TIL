RugbyBot
--------
```java
import becker.robots.*;
public class RugbyBot extends RobotSE {

 public RugbyBot(City arg0, int arg1, int arg2, Direction arg3, int number) {
  super(arg0, arg1, arg2, arg3);
  this.setLabel(number + "");
 }
	
 public void advance() {
  this.pickThing();
  for(int i=0; i<2; i++) {
   this.move();
  }
  this.putThing();
 }
	
 public void advanceLeft() {
  pickThing();
  turnLeft();
  move();
  turnRight();
  this.move();
  this.move();
  this.putThing();
 }
	
 public void advanceRight() {
  pickThing();
  this.move();
  this.move();
  turnRight();
  move();
  turnLeft();
  this.putThing();
 }
}
```
RugbyField
----------
```java
import becker.robots.City;
import becker.robots.Direction;
import becker.robots.Wall;

public class RugbyField extends City {
 public RugbyField() {
  super(7, 11);
  makeWalls(this);
 }
	
 RugbyField(int numVisibleStreets, int numVisibleAvenues) {
  super(numVisibleStreets, numVisibleAvenues);
  makeWalls(this);
 }
	
 public static void makeWalls(City city) {
  Wall[] walls = new Wall[6];
   walls[0] = new Wall(city, 3, 0, Direction.WEST);
   walls[1] = new Wall(city, 3, 0, Direction.SOUTH);
   walls[2] = new Wall(city, 3, 0, Direction.NORTH);
	      
   walls[3] = new Wall(city, 3, 10, Direction.EAST);
   walls[4] = new Wall(city, 3, 10, Direction.SOUTH);
   walls[5] = new Wall(city, 3, 10, Direction.NORTH);
 }
}
```
playingRugby
-----------
```java
import becker.robots.Direction;
import becker.robots.Thing;

public class PlayingRugby{
 public static void main(String[] args) {
  RugbyField rugbyField = new RugbyField();
  new Thing(rugbyField, 4, 9);
  RugbyBot[] team = createTeam(rugbyField);
  directs(team);
 }
	
 public static RugbyBot[] createTeam(RugbyField rugbyField) {
  RugbyBot[] rugbyBots = new RugbyBot[4];
  for(int i = 0; i < rugbyBots.length; i++) {
   if (i < 2) {
    rugbyBots[i] = new RugbyBot(rugbyField, 4-i, 9-(2*i), Direction.WEST, i+1);
   } else {
    rugbyBots[i] = new RugbyBot(rugbyField, 2, 9-(2*i), Direction.WEST, i+1);
   }
  }
  return rugbyBots;
 }
	
 public static void directs(RugbyBot[] rugbyBots) {
  for(int i = 0; i < rugbyBots.length; i++) {
   if (i < 2) {
	  rugbyBots[i].advanceRight();
   } else if ( i == 2 ) {
	  rugbyBots[i].advance();
   } else if ( i == 3 ) {
	  rugbyBots[i].advanceLeft();
   }
  }
 }
}

```
