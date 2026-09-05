# Ex12 Add Elements from an Array into a TreeSet
## DATE: 06.08.2026
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.
## Algorithm
1. Read input array
2. Create empty TreeSet
3. Insert all array elements into TreeSet
4. Print TreeSet elements (in sorted order)   

## Program:
```
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by: JAISREE N
RegisterNumber: 212224060104
*/
```
```
import java.util.*;

public class ArrayToTreeSet {

    public static TreeSet<Integer> convertArrayToTreeSet(int[] arr) {
        TreeSet<Integer> set = new TreeSet<>();
        for(int num:arr)
            set.add(num);
        return set;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        TreeSet<Integer> treeSet = convertArrayToTreeSet(arr);
        System.out.println("Elements in TreeSet:");
        for (int num : treeSet) {
            System.out.println(num);
        }

        sc.close();
    }
}
```

## Output:
<img width="655" height="558" alt="image" src="https://github.com/user-attachments/assets/ebe56097-c7ba-414e-aa85-7f2e3b6a0189" />

## Result:
The program successfully adds elements from an array into a TreeSet.
