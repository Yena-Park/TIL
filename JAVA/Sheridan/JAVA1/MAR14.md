For
===
For
---
```java
public static void main(String[] args){
  for(int i=0; i<10; i++){
    System.out.println("1 * "+i+" = "+(1*i));
  for(int i=0; i<10; i++){
    System.out.println("2 * "+i+" = "+(2*i));
  for(int i=0; i<10; i++){
    System.out.println("3 * "+i+" = "+(3*i));
  for(int i=0; i<10; i++){
    System.out.println("4 * "+i+" = "+(4*i));
  for(int i=0; i<10; i++){
    System.out.println("5 * "+i+" = "+(5*i));
  }
}
```
For Even Odd Test
-----------------
```java
public class ForEvenOddTest {
  public static void main(String[] args) {
    for (int i=1;i<=20;i++)
    {
      if (i%2 == 0 ) 
        System.out.print(i + " ");
    }
  }  
} 
```
For Square
----------
```java
public class ForSquare {
  public static void main(String[] args) {
    for (int i=1;i<=10;i++)
    {
      System.out.println(i + " " + (int)(Math.pow(i,2)));
    }
  }
}
```
For Square Reverse
------------------
```java
public class ForSquareReverse {
  public static void main(String[] args) {
    for (int i=10;i>=0;i--)
    {
      System.out.println(i + "      "     +(int)(Math.pow(i,2)));
    }
  }
}
```
For Sum Test
------------
```java
public class ForSumTest {
  public static void main(String[] args) {
    int sum = 0 ;
    int sum1= 0 ;
    for (int i=0;i<10;i++)
    {
      sum += i ;
    }

    System.out.println("sum is " +sum);

    for (int i=0;i<10;++i)
    {
      sum1 += i ;
    }
    
    System.out.println("sum 1 is " +sum1);
  }
}
```
Nested loop : For Pattern Test
----------------
```java
public static void main(String[] args) {
  for (int i=0;i<10;i++)
  {
    for(int j=1;j<=i;j++)
    {
      System.out.print("*");
    } 
    System.out.println("");
  }
}
```
Nested loop : For Reverse Pattern
---------------------------------
```java
public static void main(String[] args) {
  for(int i=0; i<10; i++){
    for(int j=10;j>i;j--) {
        System.out.print("*");
      }
   System.out.println("");
   }
}
```
Nested loop : For Five Table
----------------------------
```java
public static void main(String[] args){
  for(int i=0; i <= 5; i++){
    System.out.println("Table of " +i+" Starts here");
    for(int j=1; j<10; j++){
      System.out.println(i+"*"+j+"="+(i*j));
    }
  }
}
```
Nested loop : For from 1 to 5 Table
-----------------------------------
```java
public static void main(String[] args) {
  for(int i = 1 ; i <=5; i ++)
  { //inside for loop
    System.out.println("--------------------TABLE OF " + i +" STARTS HERE -------------");
    for (int j=1;  j<=10;   j++)
    { //child for loop
      System.out.println(i + " * " + j  + " = " + (i*j));
    } //end of child for loop
  }
}
```
Nested loop exercise 1
----------------------
```java
public static void main(String[] args) {
  for(int i=1; i<=10; i++) {
    for(int j=1; j<=i; j++) {
      System.out.print(j+" ");
    }
      System.out.println("");
    }
}
```
Nested loop exercise 2
----------------------
```java
public static void main(String[] args) {
  for(int i=10; i>=1; i--) {
    for(int j=1; j<=i; j++) {
      System.out.print(j+" ");
    }
    System.out.println("");
	}
}
```
Shifting Elements
-----------------
```java
int []myList = {0, 1, 2, 3, 4};
int temp = myList[0];
for(int i=1 ; i<myList.length; i++) {
  myList[i-1]=myList[i];
}
myList[myList.length-1]=temp;
```
