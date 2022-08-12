# Data Structures

### Hash Map
* Constant Time
* Unordered

```java
import java.util.HashSet;

HashSet<Integer> variableName = new HashSet<Integer>();

variableName.add("A");
variableName.remove("A");
boolean check = variableName.contains("A");
variableName.clear(); // remove all items
int size = variableName.size(); // how many items

// Looping through HashSet using for-each loop
for(Integer i : variableName){
  System.out.println(i);
}
```
