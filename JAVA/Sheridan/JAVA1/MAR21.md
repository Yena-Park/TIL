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
	System.out.println("Afer calling nethod 2");
}

public static void displayMethod2() {
	System.out.println("Method2");
}
```
