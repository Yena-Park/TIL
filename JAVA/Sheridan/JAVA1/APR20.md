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
