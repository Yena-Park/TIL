Array
=====
Array test and sum
------------------
```java
//1st way to declare and create
  int[] myList = new int[5];//creating
  myList[0]=10;
  myList[2]=30;
  myList[4]=50;
  //int[] myList = {10, 20, 30, 40, 50}
```		
```java
//2nd way to declare
  int[] myList = new int[5] //assigning values to array
  System.out.println("Length of my list is "+myList.length);
    
  for (int i = 0; i<myList.length; i++){
  System.out.println("My list value of position "+i+ "is "+myList[i]);
  }
```
Array test reverse and sum
--------------------------
```java
int[] myList = new int[5];//creating
  myList[0]=10;
  myList[1]=20;
  myList[2]=30;
  myList[3]=40;
  myList[4]=50
for (int i = myList. ; i>=0; i--) {
  System.out.println("My list value of position "+i+ "is "+myList[i]);
}
```
Using same array. Write a program using for loop to produce sum of all the value of ARRAY
-----------------------------------------------------------------------------------------
```java
int[] myList = new int[5];
  myList[0]=10;
  myList[1]=20;
  myList[2]=30;
  myList[3]=40;
  myList[4]=50;

int sum = 0;

for (int i = 0; i<myList.length ; i++) {
  sum = sum+myList[i];
}
System.out.println("Sum of my list is "+ sum);
```
Write a program. Ask user to enter the length of array.Once you get the length from user, declare and create the ARRAY of length given by user. Using FOR LOOP
------------------------------------------
```java
import java.util.Scanner;
public class arrayScanner {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    System.out.println("Enter the number");
    int length = input.nextInt();
    
    int[] myList = new int[length];
    int sum=0;
    for (int i = 0; i<= myList.length-1 ; i++) {
      sum=sum+myList[i];
      System.out.println("Enter integer");
      myList[i]=input.nextInt();
    }
    System.out.println("The total sum is "+sum);
}
}
```
Store values from 1 to 10 in an array. Using FOR loop print even numbers.
--------------------------------------------------------------------------
```java

```
You have 5 values in an array{33, 35, 48, 37, 56}. Find out Max value of the ARRAY
