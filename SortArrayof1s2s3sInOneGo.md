We can solve this question by counting also, by running a loop counting the frequency of any two numbers out of 3.
But here we have tried to solve it in one Go.

```
public class a7Sort123 {

    public static void main(String[] args) {
        int a[] = {1, 2, 0, 1, 0, 1, 0, 1, 0, 2, 1, 0, 2, 1, 1, 0, 2, 1, 0, 2, 0, 0, 0, 2, 0, 1, 2, 2, 0, 1, 2};

        int end = a.length - 1;
        int start = 0;
        int index = 0;

        while (index <= end) {
            if (a[index] == 0) {
                int temp = a[start];
                a[start] = a[index];
                a[index] = temp;
                start++;
            } else if (a[index] == 2) {
                int temp = a[index];
                a[index] = a[end];
                a[end] = temp;
                end--;
            } else {
                index++;
            }
        }

        for (int x : a) {
            System.out.print(x+" ");
        }

    }
}
```
Output -
 ```
 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2 2 
 ```
