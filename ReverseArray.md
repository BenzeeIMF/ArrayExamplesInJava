In this code we have reverse the array without using any extra space.

```
  public class a9ReverseArray {

    public static void main(String[] args) {
        int a[] = {12, 23, 345, 5, 56, 68, 89};

        int start = 0;
        int end = a.length - 1;

        for (int x : a) {
            System.out.print(x + " ");
        }
        while (start < end) {
            int temp = a[start];
            a[start] = a[end];
            a[end] = temp;
            end--;
            start++;
        }
        System.out.println("");
        for (int x : a) {
            System.out.print(x + " ");
        }
    }
}
 ```
 Output - 
 ```
12 23 345 5 56 68 89 
89 68 56 5 345 23 12
 ```
