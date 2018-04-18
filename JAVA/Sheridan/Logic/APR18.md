AnotherRobot
------------
```java
import becker.robots.*;
    
    public class AnotherRobot extends RobotSE {
    
        //constructor
        public AnotherRobot(City c, int st, int ave, Direction d, int t){
            super(c, st, ave, d, t);
        }
        
        //method that makes the robot turn at a certain direction (dir)
        public void faceDirection(Direction dir) {
            while(this.getDirection() != dir) {
                 this.turnLeft();
            }
        }
        
        //method that makes the robot move until it comes across a wall
        public void moveToWall(){
            while(this.frontIsClear())
                this.move();
        }
                
        //method that makes the robot drop things to create a box of certain sizes
        public void makeBox(int width, int height){
            for(int i = 0; i<height; i++){
                this.makeRow(width);
                this.nextRow();
            }
        }
        
        //make a row of things
        public void makeRow(int w){
            for(int i = 0; i < w; i++){
                this.putThing();
                this.move();
            }
        }
        
        //move to the next row and get ready to drop things for another row
        public void nextRow(){
            if (this.isFacingEast()){
                this.faceDirection(Direction.SOUTH);
                this.move();
                this.faceDirection(Direction.WEST);
                this.move();
            }else{
                this.faceDirection(Direction.SOUTH);
                this.move();
                this.faceDirection(Direction.EAST);
                this.move();
            }
        }
    }
```
