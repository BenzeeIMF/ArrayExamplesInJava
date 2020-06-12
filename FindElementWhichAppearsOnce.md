All the numbers except one number is available in even number of times(Mostly 2). We have to find the number which appears only once. 

```
public class a8FindElementWhichAppearOnce {

    public static void main(String[] args) {
        int a[] = {1, 1, 2, 2, 2, 2, 3, 4, 4, 5, 5, 6, 6};
        int number = 0;
        for (int i = 0; i < a.length; i++)
        {
            number = number ^ a[i];
        }
        System.out.println(number);
    }
}
```
Output - 
```
3
```
