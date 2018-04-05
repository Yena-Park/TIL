System.in 대신에 데이터 파일의 이름을 지정하고, File을 만든 후 그 파일에 대한 Scanner 만들기
----------------------------------------------------------------------------
```java
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;
public class Code19 {

  public static void main(String[] args) {
    String [] name = new String [1000];
    String [] number = new String[1000];
    int n = 0;
		
    try {
      Scanner inFile = new Scanner(new File("input.txt"));
			
      while(inFile.hasNext()) {   //detect End of file
        name[n] = inFile.next();
        number[n] = inFile.next();
        n++;
      }
			
      inFile.close();
    } catch (FileNotFoundException e) {
      System.out.println("No File");
      System.exit(0);
    }

    for (int i=0; i<n; i++) {
      System.out.println(name[i] +": "+number[i]);
    }
  }
}
```
