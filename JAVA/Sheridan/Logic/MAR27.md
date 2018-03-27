Make Box
========
```java
import becker.robots.*;
import java.util.Random;
public class BoxMaker {

  public static void main(String[] args) {
    /** This program uses the robot to create an 'ave' by 'st' box of things.
    * The numbers 'ave' and 'st' are randomly generated.**/

    City boxCity = new City(10, 10);
    Random generator = new Random();
    int ave = generator.nextInt(7) + 2;
    int st = generator.nextInt(7) + 2;

    System. out.print("The robot will create a " + ave + " by " + st + " box");
    Robot mark = new Robot(boxCity, 1, 1, Direction.EAST, 100);

    //call the methods
    makeBox(mark, ave, st);
  }
  
  //Create methods below this line
  private static void makeRow(Robot r, int length) {
    for(int i=0; i<length; i++) {
      r.putThing();
      r.move();
    }
  }
	
  private static void turnRight(Robot r) {
      for(int i=0; i<3; i++) {
      r.turnLeft();
    }
  }
	
  private static void nextRow(Robot r) {
    if(r.getDirection() == Direction.EAST) {
      for(int i=0; i<2; i++) {
        turnRight(r);
        r.move();
      }
    }else {
      for(int i=0; i<2; i++) {
        r.turnLeft();
        r.move();
      }
    }
  }
	
  private static void makeBox(Robot r, int length, int height) {
    for(int i=0; i<height; i++) {
      makeRow(r, length);
      nextRow(r);
    }
  }
}
```
