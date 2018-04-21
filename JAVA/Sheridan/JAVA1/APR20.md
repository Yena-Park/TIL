```java
import java.util.Scanner;

public class Circle {
 public static void main(String[] args) {

  Scanner input = new Scanner(System.in);

  System.out.print("Enter a radius: ");
  int number = input.nextInt();

  try{
   if (number==0)
   {
    throw new ArithmeticException("You can not enter radius as 0");
   }
   else if (number < 0 ) {
    throw new ArithmeticException("You cannot enter radius less than 0");
   }
   else{
    double area = number*number*3.14;
    System.out.println("the value of area is " + area);
   }
  }
  catch(Exception ex){
   System.out.println(ex);
  }
 }        
}
```

```java
import java.util.*;
public class DemoTwoCatch{
 public static void main(String[] args)
 {
  int i = 5;
  int j = 0;
  int[] myList = {10,20,30};

  try  {
   // System.out.println("i divided by j" +(i/j));
   System.out.println("element at 3rd position" +myList[3]);  
  }
  catch(ArithmeticException ex){
   System.out.println("you are in arithmetic exception");
   System.out.println(ex);
  }   
  catch(ArrayIndexOutOfBoundsException ex){
   System.out.println("you are in ArrayIndexOutofBound exception");
   System.out.println(ex);
  }
  System.out.println("Execution continue...");
 }
}
```
