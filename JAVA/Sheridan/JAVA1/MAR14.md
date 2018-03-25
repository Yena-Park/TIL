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
For Five Table
--------------
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
For Pattern Test
----------------
```java
public static void main(String[] args) {
  for(int i=0; i<=10; i++){
    for(int j=1; j<=i; j++) {
      System.out.print("*");
    }
        System.out.println("*");
}
```
For Reverse Pattern
-------------------
```java
public static void main(String[] args) {
  for(int i=10; i>=1; i--){
    for(int j=0;j<=i-1;j++) {
        System.out.print("*");
      }
   System.out.println("*");
   }
}
```
```java
public static void main(String[] args) {
  for(int i=0; i<=10; i++){
    for(int j=10;j>=i;j--) {
        System.out.print("*");
      }
   System.out.println("*");
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
