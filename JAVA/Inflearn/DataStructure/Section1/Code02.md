```java
import java.util.Scanner;
public class Code02 {
	public static void main(String[] args) {
		int number = 123;
		int keyboard;
		
		Scanner input = new Scanner(System.in);
		System.out.println("Please enter an integer: ");
		keyboard = input.nextInt();
		
		if(keyboard == number)
			System.out.println("Numbers match!");
		else
			System.out.println("Numbers do not match");
	}

}
```
