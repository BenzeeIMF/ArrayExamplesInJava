This code has a time complexity of O(n) and space complexity of O(1)

```
public class SecondSmallestNumber {

    public static void main(String[] args) {

        int a[] = {1, 12, 23, 543, 17, 52, 97, 40, 34};
        int smallest = Integer.MAX_VALUE;
        int secondSmallest = Integer.MAX_VALUE;

        for (int i = 0; i < a.length; i++) {
            if (a[i] < smallest) {
                smallest = a[i];
            }
            if (a[i] < secondSmallest && a[i] > smallest) {
                secondSmallest = a[i];
            }
        }
        System.out.println(smallest);
        System.out.println(secondSmallest);
    }
}
```
Output - 
```
1
12
```
