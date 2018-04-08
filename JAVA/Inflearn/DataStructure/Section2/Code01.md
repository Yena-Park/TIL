```java
public static void main(String[] args) {
  Person1 first;
  first = new Person1();
		
  first.name = "John";
  first.number="010202049498";
		
  System.out.println("Name: " + first.name + ", Number: " + first.number);
		
  Person1[] members = new Person1 [100];
  members[0] = first;
  members[1] = new Person1();
  members[1].name = "David";
  members[1].number = "0104546987320";
		
  System.out.println("Name: " + members[1].name + ", Number: " + members[1].number);
}
```
