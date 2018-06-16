```java
public class Start
{
  public static void main (String[] args)
  {
      Person p1 = new Person("Rich");
      Student s1 = new Student("Bart");
      CollegeStudent s2 = new CollegeStudent("Lisa");
      p1.eat();
      s1.study();
      s1.writeTest();
      s2.study();
      s2.writeTest();
      s2.doAssignement();
      s2.study(5);
  }
}
```
```java
public class Person
{
  protected String name;

  public Person (String name)
  {
    this.name = name;
  }

  public void eat ()
  {
    System.out.println("Yummy!!!");
  }

  public void speak (String sentence)
  {
    System.out.println(this.name + " says: " + sentence);
  }
}
```
```java
public class Student extends Person
{
  public Student (String name)
  {
    super(name);
  }
```
```java
public class CollegeStudent extends Student //need to inherit study and writeTest from Student
{
  public CollegeStudent (String name)
  {
    super(name);
  }

  //CollegeStudents also need to be able to doAssignments

  public void doAssignement ()
  {
    System.out.println(this.name + " is doing an assignment");
  }

  //overload study to allow you to pass an int for the number of hours to study

  public void study (int numHours)
  {
    for (int hours = 0; hours < numHours; hours++) {
      System.out.println(this.name + " is studying...hour " + hours);
    }
  }
}
```
