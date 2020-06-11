This code has a time complexity of O(n) and space complexity of O(1).
We can use hashmaps for solving this program.

```
public class PairsWithGivenSum {

    public static void main(String[] args) {

        int a[] = {1, 2, 3, 5, 6, 10, 13, 14, 16, 17, 20};
        int sum = 16;

        int start = 0;
        int end = a.length - 1;

        while (start < end) {

            if (a[start] + a[end] < sum) {
                start++;
            } else if (a[start] + a[end] > sum) {
                end--;
            } else {
                System.out.println(a[start++] + " " + a[end--]);
            }
        }
    }
}
```
Output - 
```
2 14
3 13
6 10
```
