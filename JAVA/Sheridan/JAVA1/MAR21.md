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
In your main mothod print Hello. And in your own custom method ask user to enter his/her name and print it. Call the custo method from  main method.
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
