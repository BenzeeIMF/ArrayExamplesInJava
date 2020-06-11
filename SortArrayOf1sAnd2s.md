This code has a time complexity of kind of O(n) and space complexity of O(1)

```
public class SortArrayOf1sAnd0s {
    public static void main(String[] args) {
        int a[] = {1, 0, 1, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1, 0, 1, 1, 0, 1, 0, 1};
//      int a[] = {1, 0, 1, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1, 0, 1, 1, 0, 1, 0, 1};
//      int a[] = {s, 0, 1, 0, 1, 1, 0, 1, 0, 1, 0, 0, 1, 0, 1, 1, 0, 1, e, 1};

        int start = 0;
        int end = a.length - 1;
        int index = 0;
        while (index < end) {
            if (a[index] == 1) {
                int temp = a[end];
                a[end] = a[index];
                a[index] = temp;
                end--;
            } else {
                int temp = a[index];
                a[index] = a[start];
                a[start] = temp;
                start++;
                index++;
            }
        }
        for (int i = 0; i < a.length; i++) {
            System.out.print(a[i] + " ");
        }
    }
}

```
Output -
```
0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 1
```
