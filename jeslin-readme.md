# Problem-statement:
### Longest Common Subsequence
#### Example 1:
```
Input: text1 = "abcde", text2 = "ace" 
Output: 3  
Explanation: The longest common subsequence is "ace" and its length is 3.
```
#### Example 2:
```
Input: text1 = "abc", text2 = "abc"
Output: 3
Explanation: The longest common subsequence is "abc" and its length is 3.
```
#### Example 3:
```
Input: text1 = "abc", text2 = "def"
Output: 0
Explanation: There is no such common subsequence, so the result is 0.
```
# Program:
##### Java
```
import java.util.Scanner;
public class Main {
    public int longestCommonSubsequence(String text1, String text2) {
        int m = text1.length();
        int n = text2.length();
        int arr[][] = new int[m + 1][n + 1];

        for (int i = 1; i <= m; i++) {
            for (int j = 1; j <= n; j++) {
                if (text1.charAt(i - 1) == text2.charAt(j - 1)) {
                    arr[i][j] = 1 + arr[i - 1][j - 1];
                } else {
                    arr[i][j] = Math.max(arr[i][j - 1], arr[i - 1][j]);
                }
            }
        }
        return arr[m][n];
    }
    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        String text1 = scanner.nextLine();
        String text2 = scanner.nextLine();
        Main solution = new Main();
        int result = solution.longestCommonSubsequence(text1, text2);

        System.out.println("Longest Common Subsequence Length: " + result);
    }
}


```
# Output:
![Screenshot 2025-03-24 143427](https://github.com/user-attachments/assets/79a63de8-3c4b-4c87-8e71-56dd5c691168)
