
```
public class PrintDuplicatesUsingSets {

    public static void main(String[] args) {

        int a[] = {1, 2, 3, 1, 2, 4, 1, 5, 2, 4, 1};
        Set<Integer> set = new HashSet<>();

        for (int i = 0; i < a.length; i++) {
            set.add(a[i]);    
      //SETS ONLY ALLOWED UNIQUE VALUES
        }

        System.out.println(set);
    }
}
```
Output -
```
[1, 2, 3, 4, 5]
```
