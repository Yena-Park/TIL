Method
======
Display Java
------------
```java
public static void main(String[] args) {
  displayJavaMethod(); //calling of Method
  System.out.println("Bye...");
  }
	
public static void displayJavaMethod() {
  System.out.println("Hello Java...");
}
```
```java
public static void main(String[] args) {
  System.out.println("Bye...");
  }
	
public static void displayJavaMethod() {
  System.out.println("Hello Java...");
}
```
```java
public static void main(String[] args) {
  for(int i=0;i<10; i++){
    displayJavaMethod();
  }
}
	
public static void displayJavaMethod() {
  System.out.println("Hello Java...");
}
```
```java
public static void main(String[] args) {
  displayJavaMethod();
  System.out.println("Bye");
}

public static void displayJavaMethod() {
  System.out.println("Hello Java...");
  displayMethod2();
  System.out.println("Afer calling Method 2");
}

public static void displayMethod2() {
  System.out.println("Method2");
}
```
In your main method print Hello. And in your own custom method ask user to enter his/her name and print it. Call the custo method from  main method.
---------------------------------------------------------------------------------------------------------------------------
```java
import java.util.Scanner;
public class displayNameHello {

  public static void main(String[] args) {
    displayJavaMethod();
    System.out.println("Hello");
  }

  public static void displayJavaMethod(){
    Scanner input = new Scanner(System.in);
    System.out.println("Enter your name");
    String name = input.nextLine();
    System.out.println(name);
  }
}
```
Calculate Area
--------------
```java
public static void main(String[] args) {
  calculateArea(10);
  calculateArea(20);
  calculateArea(40);
}

public static void calculateArea(int r) {
  double area = 3.14*r*r;
  System.out.println("Area is "+area);
}
```
Create a method to print table as below for the number given in parameter of the method. Make sure you use FOR LOOP to print below table. Let us assume that number in parameter is 5. Then print 5 * 1 = 5   5 * 2 = 10 ... 5 * 10 = 50 
-----------------------------------------------------------------------------------------------------------------------------
```java
public static void main(String[] args) {
  makeTable(5);
}
		
public static void makeTable(int r) {
  for(int i=1; i<=10; i++) {
  int result = 5*i;
  System.out.println("5 * "+i+" = "+result);
}
```
Make table
----------
```java
import java.util.Scanner;
public class practice {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    System.out.println("Enter int");
    int num = input.nextInt();
    makeTable(num);
  }
  public static void makeTable(int i) {
    for(int j=1; j<=10; j++) {
    System.out.println(i+" * "+j +" = "+ (i*j));
    }
  }
}
```
Sum
---
```java
  public static void main(String[] args) {
    calculateSum(5, 4.5);
  }
  public static void calculateSum(int a, double b) {
    double sum = a+b;
    System.out.println("sum is "+sum);
  }
```
More Sum
--------
```java
  public static void main(String[] args) {
    double calculateSum(5, 4.5, 10, 20);
    System.out.println("Value of d is "+d);
  }
  public static void calculateSum(int a, double b) {
    double sum = a+b+c+d;
    System.out.println("sum is "+sum);
```
