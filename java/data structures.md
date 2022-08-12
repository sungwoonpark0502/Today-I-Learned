# Data Structures

### HashSet
* Constant Time
* Unordered
* No duplicates allowed

```java
import java.util.HashSet;
import java.util.Iterator;

HashSet<Integer> set = new HashSet<Integer>();

set.add("A");
set.remove("A");
boolean check = set.contains("A");
set.clear(); // remove all items
int size = set.size(); // how many items

// Looping through HashSet using for-each loop
for(Integer i : set){
  System.out.println(i);
}

// Using Iterator
Iterator iter = set.iterator();
while(iter.hasNext()){
  System.out.print(iter.next() + " "); // if set = [1,2,5], result: 1 2 5
}
```
