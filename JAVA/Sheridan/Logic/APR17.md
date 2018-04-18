```java
import becker.robots.*;

public class Sweeper {
    
   public static void main(String[] arg) {
      // Problem setup
      City city = new City();
      RobotSE karel = new RobotSE(city, 0, 0, Direction.WEST);
      createThings(city);
      
      // ****** Write your method call(s) bellow ******
      int st = 5; int ave = 5;
      System.out.print("Total nummber of things: " + sweep(karel, st, ave));
   }
   
   //create things in the city
   private static void createThings(City anyCity){
      Thing t1 = new Thing(anyCity, 1, 2);
      for (int ave = 1; ave<=3; ave++){
          Thing t2 = new Thing(anyCity, 2, ave);
      }
      for (int ave = 0; ave<5; ave++){
          Thing t2 = new Thing(anyCity, 3, ave);
      }
       for (int ave = 1; ave<=3; ave++){
          Thing t2 = new Thing(anyCity, 4, ave);
      }
      Thing t8 = new Thing(anyCity, 5, 2);
   }
  
   //method for positioning the robot and picking and adding up the things of each row
   private static int sweep(RobotSE r, int s, int a){
       int totalThings = 0;
       for(int i = 0; i < s; i++){
           takePosition(r);
           totalThings = totalThings + sweepStreet(r, a);
       }
       return totalThings;
   }
   
   //method for positioning the robot before continuing to the next row
   private static void takePosition(RobotSE rob){
       if(rob.isFacingWest()){
           rob.turnLeft();
           rob.move();
           rob.turnLeft();
       }else{
           rob.turnRight();
           rob.move();
           rob.turnRight();
       }
   }
    
   //method for picking up the things in a single row
   private static int sweepStreet(RobotSE r, int avenues){
       int things = 0;
       for(int i = 0; i<avenues; i++){
           if(r.canPickThing()){
               r.pickThing();
               things++;
           }
           r.move();
       }
       return things;
   }
}
```
