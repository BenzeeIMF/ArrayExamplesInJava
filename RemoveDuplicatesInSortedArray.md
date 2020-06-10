In this code, we have removed the elements from Sorted Array in O(1) space complexity and O(n) time complexity

```
public class RemoveDuplicateFromSortedArray {

    public static void main(String[] args) {

        int a[] = {1, 1, 2, 3, 4, 5, 6, 6, 6, 7};
        int j = 0;
        for (int i = 0; i < a.length - 1; i++) {
            if (a[i] != a[i + 1]) {
                a[j++] = a[i];
            }
        }
        a[j] = a[a.length - 1];

        for (int i = 0; i < j; i++) {
            System.out.print(a[i]+" ");
        }
    }
}
```

OUTPUT 
```
1 2 3 4 5 6
```
