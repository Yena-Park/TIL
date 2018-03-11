```java
import java.util.Scanner;
public class Code09 {
	public static void main(String[] args) {
		int n;
		Scanner input = new Scanner(System.in);
		n = input.nextInt();
		int[] data = new int[n];
		
		for(int i=0; i<n; i++)
			data[i]=input.nextInt();
		input.close();
		
		int tmp = data[n-1];
		
		for(int i=n-2; i>=0; i--)
			data[i+1]=data[i];
		data[0]=tmp;
		
		for(int i=0; i<n; i++)
			System.out.println(data[i]);
	}
}
```
