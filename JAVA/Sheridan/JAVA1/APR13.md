
```java
public class Student {
 private String firstName;
 private String lastName;
 private int studentId;
	
 public Student() {
  firstName = "a";
  lastName = "a";
  studentId = 1;
	}
	
	public Student(String fName, String lName, int sId) {
		firstName = fName;
		lastName = lName;
		studentId = sId;
	}
	
	public void setfirstName(String f1) { //f1 is parameter, 처음에 private variable이어서, get&set이 필요.
		firstName = f1;
	}
	
	public String getfirstName() {
		return firstName;
	}

	public void setsecondName(String f2) {
		lastName = f2;
	}
	
	public String getlastName() {
		return lastName;
	}
	
	public void setstudentId(int sId) {
		studentId = sId;
	}
	
	public int getstudentId() {
		return studentId;
	}
}

```
```java
public class testStudent {
	public static void main(String[] args) {
		Student s1 = new Student();
		
		Student s2 = new Student("Ronak", "Sheth", 100);
		
		s1.setfirstName("Yena");
		s1.setlastName("Park");
		s1.setstudentId(200);
		
		System.out.println("first name of student s2 is "+s2.getfirstName());
		System.out.println("last name of student s2 is "+s2.getlastName());
		System.out.println("student ID of student s2 is "+s2.getstudentId());
		
		System.out.println("first name of student s2 is "+s1.getfirstName());
		System.out.println("last name of student s2 is "+s1.getlastName());
		System.out.println("student ID of student s2 is "+s1.getstudentId());
	}
}
```
