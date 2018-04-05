```java
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;
public class Code20 {
	
  static String [] name = new String [1000];  //하나의 Class는 여러개의 method로 구성되는데, 2개 이상의 method(함수)에서 공통으로 사용하는 변수는 method 밖에 선언가능(Class member)
  static String [] number = new String[1000];
  static int n = 0;

  public static void main(String[] args) {
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
    bubbleSort();
    for (int i=0; i<n; i++) {
      System.out.println(name[i] +": "+number[i]);
    }
  }
	
  static void bubbleSort() {
    for(int i=n-1; i>0; i--) {
      for(int j=0; j<i; j++) {
      if(name[j].compareTo(name[j+1]) > 0) {  //str1.equals(str2)이렇게 해야함.  str1 == str2 <-이렇게 하면 안됨. name[j]가 더 앞순서 알파벳이면 양수 리턴.
        String tmp = name[j];
        name[j] = name[j+1];
        name[j+1]=tmp;
					
        tmp = number[j];
        number[j] = number[j+1];
        number[j+1]=tmp;
      }
    }
  }
 }
}
```
