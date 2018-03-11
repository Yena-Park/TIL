```java
import java.util.Scanner;
public class Code08 {
	public static void main(String[] args) {
		int n;

		Scanner input = new Scanner(System.in);
		n = input.nextInt();
		int[] data = new int [n];

		for (int i=0; i<n; i++)
			data[i]=input.nextInt();
		input.close();

		int sum = 0, max = data[0];
		for (int i=0; i<n; i++) {
			sum += data[i];
			if (data[i]>max) max = data[i];
		}
		System.out.println("The sum is "+sum+" and the maximum is "+max);
	}
}
```
