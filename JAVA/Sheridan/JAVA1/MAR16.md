Array
=====
Array Scanner
-------------
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
      System.out.println("Enter integer");
      myList[i]=input.nextInt();
      sum=sum+myList[i];
    }
   System.out.println("The total sum is "+sum);
  }
}
```
Array Input
-----------
```java
import java.util.Scanner;
public class Excercise {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
      System.out.println("Enter length of Array");
      int length = input.nextInt();
		
      int[] myList = new int[length];
      int value = 0;
      for(int i=0; i<length; i++) {
        System.out.println("Enter value "+i+" position");
        myList[i] = input.nextInt();
      }
      System.out.println("Printing Array");
      System.out.println("--------");
      for(int i=0; i<length; i++) {
        System.out.println(i+" position value is "+myList[i]);
      }
  }
}
```
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
for (int i = myList.length; i>=0; i--) {
  System.out.println("My list value of position "+i+ "is "+myList[i]);
}
```
Array test for odd number and even number
-----------------------------------------
```java
public static void main(String[] args) {
  int[] myList = {2,10,30,8,5};
  for (int i = 0 ;i<myList.length; i++){    
    if (myList[i]%2 ==0)
      System.out.println(myList[i] +"is Even number");
    else 
      System.out.println(myList[i] +"is odd number");
  }
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
Write a program. Ask user to enter the length of array.Once you get the length from user, declare and create the ARRAY of length given by user. And then find the sum of all array. Using FOR LOOP
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
----------------------------------------------------------------------------------
```java
public static void main(String[] args) {
  int[] myList = {2, 10, 30, 8, 5};

  for(int i=0; i<myList.length; i++) {
  if (myList[i]%2 == 0)
    System.out.println(myList[i]+" is Even number");
  else
    System.out.println(myList[i]+" is Odd number");
  }
}
```
Ask user to enter number of student. Ask user to enter total marks for each student. Now print Grade for all the students. Total marks>90 then print "A", Total marks>80 then print "B", Total marks>70 then "C", Total marks>60 then "D" and Total marks>50 then print "E".
-------------------------------------------------------------------------------------------------------------------------
```java
import java.util.Scanner;
public class arrayStudentGrade {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    System.out.println("Enter the number student");
    int length = input.nextInt();
    int[] myList = new int[length];
		
    for(int i=0; i<myList.length; i++) {
      System.out.println("Enter the marks");
      myList[i] = input.nextInt();
    }
		
    for(int i=0; i<myList.length; i++) {
      if (myList[i]>=90) {
        System.out.println(myList[i]+" is A");}
      if (myList[i]>=80 && myList[i]<90) {
        System.out.println(myList[i]+" is B");}
      if (myList[i]>=70 && myList[i]<80) {
        System.out.println(myList[i]+" is C");}
      if (myList[i]>=60 && myList[i]<70) {
        System.out.println(myList[i]+" is D");}
      if (myList[i]<50) {
        System.out.println(myList[i]+" is E");}
	
      }

  }

}
```
Ask user to enter length. Get Int numbers from user. Find average for all the numbers.
-------------------------------------------------------------------------------------
```java
import java.util.Scanner;
  public class arrayUserAverage {
    public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      System.out.println("Enter the length");
        int length = input.nextInt();
        int[] myList = new int[length];

        for(int i=0; i<myList.length; i++) {
        System.out.println("Enter the value as integer");
        myList[i] = input.nextInt();
        }
    
        int sum = 0;
        for(int i=0; i<myList.length; i++) {
          sum = sum+myList[i];
        }

        double average = sum/length;
        System.out.println("Average is "+average);
  }
}
```
