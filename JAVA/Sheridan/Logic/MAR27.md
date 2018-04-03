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
Diamond problem
---------------
```java
package WeekNine;

import becker.robots.*;
import java.util.Random;

public class DiamondProblem {
	public static void main(String[] arg) {

		//problem setup
		City diamondCity = new City(12,12);
		Robot roby = new Robot(diamondCity, 5, 9, Direction.NORTH, 100);
		int side = 4;
		//method call
		makeDiamond(roby, side);
	}

	//method for making a diamond
	private static void makeDiamond(Robot r, int s){
		for (int i =0; i <4; i++){
			diamondSide(r, s);
			positionForNextSide(r);
		}
	}

	//method for making one side of the diamond
	private static void diamondSide(Robot r, int s){
		for(int i = 0; i <s; i++){
			r.putThing();
			r.move();
			r.turnLeft();
			r.move();
			turnRight(r);
		}
	}

	//move and position the robot for the next side	
	private static void positionForNextSide(Robot r){
		turnAround(r);
		r.move();
		turnRight(r);
	}

	//method for making the robot turn right
	private static void turnRight(Robot r){
		for (int i =0; i<3; i++){
			r.turnLeft();
		}  
	}

	//method for making the robot turn around
	private static void turnAround(Robot r){
		for (int i =0; i<2; i++){
			r.turnLeft();
		}
	}
}
```
Hub problem
-----------
```java
package WeekNine;

import becker.robots.*;
import java.util.Random;

public class HubProblem {
	public static void main(String[] arg) {

		//problem setup
		City oakville = new City(15,15);
		Robot roby = new Robot(oakville, 7, 7, Direction.EAST);      
		//generate spokes in each direction
		generateSpokes(Direction.NORTH, oakville);
		generateSpokes(Direction.EAST, oakville);
		generateSpokes(Direction.SOUTH, oakville);
		generateSpokes(Direction.WEST, oakville);

		//assign an integer to store the value returned from your returning method
		int northSpoke = clearSpoke(roby, Direction.NORTH);
		int eastSpoke = clearSpoke(roby, Direction.EAST);
		int southSpoke = clearSpoke(roby, Direction.SOUTH);
		int westSpoke = clearSpoke(roby, Direction.WEST);

		//print out the number returned from the method together with a string explaining what the number is
		System.out.println ("The west spoke had " + westSpoke + " things");
		System.out.println ("The north spoke had " + northSpoke + " things");
		System.out.println ("The east spoke had " + eastSpoke + " things");
		System.out.print ("The south spoke had " + southSpoke + " things");
	}  
	//method for creating the spokes
	private static void generateSpokes(Direction dir, City city){
		Random generator = new Random();
		int things = generator.nextInt(10);
		if (dir == Direction.NORTH){
			for (int i = 7;  i > 7 - things; i--){
				Thing tn = new Thing(city, i - 1 , 7);
			}
		}else if (dir == Direction.WEST){
			for (int i = 7; i< 7 + things; i++){
				Thing tw = new Thing(city, 7, i + 1);
			}
		}else if (dir == Direction.SOUTH){
			for (int i = 7; i< 7 + things; i++){
				Thing ts = new Thing(city, i + 1, 7);
			}
		}else{
			for (int i = 6; i > 7 - things; i--){
				Thing te = new Thing(city, 7 , i);
			}
		}
	}

	//method for picking picking up and counting things in a certain direction
	private static int clearSpoke(Robot sweeper, Direction dir){
		faceDirection(sweeper, dir);
		int things = pickAndCount(sweeper);
		turnAround(sweeper);
		moveBack(sweeper, things);

		return things;
	}

	//method for turning the robot around
	private static void turnAround(Robot bot){
		for (int i = 0; i<2; i++)
			bot.turnLeft();
	}

	//method for moving the robot back to its original position
	private static void moveBack(Robot bot, int steps){
		for(int i = 0; i<steps + 1; i++)
			bot.move();
	}

	//method for facing the robot to a particular direction
	private static void faceDirection(Robot r, Direction dir){
		while(r.getDirection() != dir)
			r.turnLeft();
	}

	//method for picking and counting the things
	private static int pickAndCount(Robot r){
		int things = 0;
		r.move();
		while(r.canPickThing()){
			r.pickThing();
			things++;
			r.move();
		}
		return things;
	}
}
```
