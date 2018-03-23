String
======
below exmple is how to concatenate string using + sign
------------------------------------------------------
```java
  String s1 = "Hello All";
  String s2 = "We are going to learn about String";
  String s3 = "today";
  System.out.println(s1+s2+s3);
}
```
below example is how to concatenate string without using + sign
---------------------------------------------------------------
```java
System.out.println("I'm Yena "+"I will take Java class");
```
below exmample is using concat method
-------------------------------------
```java
  String s4 = "Good evening";
  String s5 = " today is Wednesday";
  String s6 = s4.concat(s5);
  String s7 = s4.concat(" this is string");
  System.out.println(s6);
  System.out.println(s7);
```
caculating length
-----------------
```java
  System.out.println("length of string  s5 is "+s5.length());    
```
character set
-------------
```java
  String s8 = "Monday";
  int i = s8.length();
  System.out.println("length of string s8 is "+i);
  
  System.out.println("Character at position 2 in s8 is "+s8.charAt(3));
  System.out.println(s8.toUpperCase());
  System.out.println(s8.toLowerCase())
```
substring
---------
```java
  System.out.println(s8.substring(0, 1));
  System.out.println(s8.substring(2, 5));
```
getting input from console
--------------------------
```java  
  Scanner input = new Scanner(System.in);
  System.out.println("Enter the value for String ");
  String s9 = input.nextLine();
  System.out.println(s8);
```  
using next method for word separated by spaces
----------------------------------------------
```java
  Scanner input = new Scanner(System.in);
  System.out.println("Enter the value for 3 words separated by spaces ");
  String s10 = input.next();
  String s11 = input.next();
  String s12 = input.next();
  System.out.println(s10+s11+s12);
```
converting string in int
------------------------
```java
  Scanner input = new Scanner(System.int);
  System.out.println("Enter first number which will stored as String");
  String s13 = input.nextLine();
  int k = Integer.parseInt(s13);
  System.out.println("Enter second numver which will stored as String");
  String s14 = input.nextLine();
  int l = Integer.parseInt(s14);
  System.out.println("Sum of two numbers are "+(k+l));
```
string comparison
-----------------
```java
  Scanner input = new Scanner(System.in);
  String s14 = "Monday";
  String s15 = "Monday";
  System.out.println("Comparison using == sign method is "+(5 == 5);
  System.out.println("Comparison using == sign method is "+(s14 == s15));
  System.out.println("Comparison using equals method is "+(s14.equals(s15)));
```
  
  
  
  
