# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE: 21.02.2026
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start the program.
2. Read an integer n (the number of inputs in the stream).
3. Create an empty LinkedHashMap<Integer, Integer> named map.
4. Repeat the following steps for each of the n numbers.
5. After processing all numbers, end the program.

## Program:
```
/*
Program to tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
```
```
import java.util.*;
public class FirstUniqueNumberStream {
    public static void processStream(int n, Scanner sc) {
        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();
        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            map.put(num, map.getOrDefault(num, 0) + 1);
            Integer firstUnique = null;
        for (int key : map.keySet()) {
            if (map.get(key) == 1) {
                firstUnique = key;
                break;
            }
        }
        if (firstUnique == null)
            System.out.println("No unique number");
        else
            System.out.println("First unique number: " + firstUnique);
    }
}
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        processStream(n, sc);
        sc.close();
    }
}
```

## Output:
<img width="696" height="622" alt="image" src="https://github.com/user-attachments/assets/fef51a3d-b393-4323-8011-a2dd3f0f89b2" />

## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.
