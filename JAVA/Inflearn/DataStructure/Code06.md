```java
public class Code06 {
	public static void main(String[] args) {
		int [] grades;
		
		grades = new int [5];
		
		grades[0] = 100;
		grades[1] = 76;
		grades[2] = 92;
		grades[3] = 95;
		grades[4] = 14;
		
		for(int i = 0; i < grades.length; i++) {
			System.out.println("Grades"+ (i)+":"+grades[i]);
		}
	}

}
```
