Person
------
```java
public class Person {
 private String firstName;
 private String lastName;
 private double weight;
 private double height;
	
 public Person() {
  firstName = "a";
  lastName = "a";
  weight = 1;
  height = 1;
 }
	
 public Person(String fName, String lName, double wgt, double hgt) {
  firstName = fName;
  lastName = lName;
  weight = wgt;
  height = hgt;
 }
	
 public Person(double wgt, double hgt) {
  weight = wgt;
  height = hgt;
 }
	
 public void setfirstName(String f1) { //f1 is parameter, 처음에 private variable이어서, get&set이 필요.
  firstName = f1;
 }
	
 public String getfirstName() {
  return firstName;
	
 public void setlastName(String l2) {
  lastName = l2;
 }
	
 public String getlastName() {
  return lastName;
 }
	
 public void setweight(double wgt) {
  weight = wgt;
 }
	
 public double getweight() {
  return weight;
 }
 public void setheight(double hgt) {
  height = hgt;
 }
	
 public double getheight() {
  return height;
 }
	
 public void calculateBMI() {
  double kilo = weight/0.453;
  double meter = height/0.0254;;
 }
}
```
Test Person
-----------
```java
public class testPerson {
 public static void main(String[] args) {
   Person p1 = new Person();

   Person p2 = new Person(50, 1.6);

   Person p3 = new Person("Yena", "Park", 50, 1.6);
		
   p1.setfirstName("ABC");
   p1.setlastName("XYZ");
   p1.setweight(100);
   p1.setheight(1.9);
		
   p2.setweight(70);
   p2.setheight(1.8);

   System.out.println("first name of p1 is "+p1.getfirstName());
   System.out.println("last name of p1 is "+p1.getlastName());
   System.out.println("weight of p1 is "+p1.getweight());
   System.out.println("height of p1 is "+p1.getheight());
   System.out.println("BMI of p1 is "+((p1.getweight()*0.435)/(p1.getweight()*0.0254)));
   System.out.println("-------------------------------------------");
   System.out.println("first name of p2 is "+p2.getfirstName());
   System.out.println("last name of p2 is "+p2.getlastName());
   System.out.println("weight of p2 is "+p2.getweight());
   System.out.println("height of p2 is "+p2.getheight());
   System.out.println("BMI of p2 is "+((p2.getweight()*0.435)/(p2.getweight()*0.0254)));
   System.out.println("-------------------------------------------");
   System.out.println("first name of p3 is "+p3.getfirstName());
   System.out.println("last name of p3 is "+p3.getlastName());
   System.out.println("weight of p3 is "+p3.getweight());
   System.out.println("height of p3 is "+p3.getheight());
   System.out.println("BMI of p3 is "+((p3.getweight()*0.435)/(p3.getweight()*0.0254)));
  }
}
```
