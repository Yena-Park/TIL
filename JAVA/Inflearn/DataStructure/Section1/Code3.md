```java
import java.util.Scanner;
public class Code03{
	public static void main(String[] args) {
		String str = "Hello";
		String input = null;
		Scanner keyboard = new Scanner(System.in);
		System.out.println("Please type a string");
		
		input = keyboard.next();
		
		if(str.equals(input)) //==을 써도 성립하지 않는다. String은 프리미티브 타입이 아니기 때문에. 
			System.out.println("Strings match!");
		else
			System.out.println("Strings do not match");
		
	}
}
```
