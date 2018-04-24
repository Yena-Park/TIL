```java
import becker.robots.*;
import java.util.Random;

public class GoToA { //PART A. 원하는 방향을 로봇이 보기 전까지 turnLeft 시키는 Method.
	public static void main(String[] arg) {
		//problem setup
		City city = new City(10,10);
		Random generator = new Random();
		int ave = generator.nextInt(10);
		int st = generator.nextInt(10);

		Robot roby = new Robot(city, st, ave, Direction.NORTH); 
		Intersection desiredIntersection = new Intersection(city, 1, 1);

		//Call the methods here
		faceDirection(roby, Direction.EAST);

	}

	//Create methods below this line
	private static void faceDirection(Robot r, Direction dir) {
		while(r.getDirection()!=dir) {
			r.turnLeft();
		}
	}
}
```
```java
import becker.robots.*;
import java.util.Random;

public class GoToB {
	public static void main(String[] arg) {
		//problem setup
		City city = new City(10,10);
		Random generator = new Random();
		int ave = generator.nextInt(10);
		int st = generator.nextInt(10);

		Robot roby = new Robot(city, st, ave, Direction.NORTH); 
		Intersection desiredIntersection = new Intersection(city, 1, 1);

		//Call the methods here
		gotoAvenue(roby, 1);
		gotoStreet(roby, 1);
	}

	//Create methods below this line
	private static void faceDirection(Robot r, Direction dir) {
		while(r.getDirection() != dir) {
			r.turnLeft();
		}
	}
	
	private static void gotoAvenue(Robot r, int avenue) {
		if(r.getAvenue() < avenue) {
			faceDirection(r, Direction.EAST);
		}else {
			faceDirection(r, Direction.WEST);
		}
		while(r.getAvenue() != avenue) {
			r.move();
		}
	}
	
	private static void gotoStreet(Robot r, int street) {
		if(r.getStreet()<street) {
			faceDirection(r, Direction.SOUTH);
		}else {
			faceDirection(r, Direction.NORTH);
		}
		while(r.getStreet() != street) {
			r.move();
		}
	}
}
```
```java
import becker.robots.*;
import java.util.Random;

public class GoToC {
	public static void main(String[] arg) {
		//problem setup
		City city = new City(10,10);
		Random generator = new Random();
		int ave = generator.nextInt(10);
		int st = generator.nextInt(10);

		Robot roby = new Robot(city, st, ave, Direction.NORTH); 
		Intersection desiredIntersection = new Intersection(city, 1, 1);

		//Call the methods here
		gotoIntersection(roby, desiredIntersection);
	}

	//Create methods below this line
	private static void faceDirection(Robot r, Direction dir) {
		while(r.getDirection() != dir) {
			r.turnLeft();
		}
	}
	
	private static void gotoAvenue(Robot r, int avenue) {
		if(r.getAvenue()<avenue) {
			faceDirection(r, Direction.EAST);
		}else {
			faceDirection(r, Direction.WEST);
		}
		while(r.getAvenue() != avenue) {
			r.move();
		}
	}
	
	private static void gotoStreet(Robot r, int street) {
		if(r.getStreet()<street) {
			faceDirection(r, Direction.SOUTH);
		}else {
			faceDirection(r, Direction.NORTH);
		}
		while(r.getStreet() != street) {
			r.move();
		}
	}
	
	public static void gotoIntersection(Robot r, Intersection inter) {
		gotoAvenue(r, inter.getAvenue());
		gotoStreet(r, inter.getStreet());
	}
}
```
