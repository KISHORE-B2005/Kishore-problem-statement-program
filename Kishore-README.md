# Problem-statement:
### Implement pow(x, n), which calculates x raised to the power n (i.e., xn).
#### Example 1:
```
Input: x = 2.00000, n = 10
Output: 1024.00000
```
#### Example 2:
```
Input: x = 2.10000, n = 3
Output: 9.26100
```
#### Example 3:
```
Input: x = 2.00000, n = -2
Output: 0.25000
```
# Program:
##### Java
```
import java.util.Scanner;
public class Main {
    public double myPow(double x, int n) {
       return Math.pow(x,n);  
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); 
        double x = scanner.nextDouble(); 
        int n = scanner.nextInt(); 
        Main solution=new Main();
        double result = solution.myPow(x, n); 
        System.out.printf("%.5f\n", result); 
        scanner.close();
    }
}
```
# Output:
![image](https://github.com/user-attachments/assets/265db22c-1764-4e80-b4e5-857315ac3eec)
