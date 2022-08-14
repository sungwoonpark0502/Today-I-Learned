# Linked List

* Each data is called "Node"


```java
import java.util.LinkedList;

LinkedList<Integer> l1 = new LinkedList<Integer>();
LinkedList<String> l2 = new LinkedList<String>();
LinkedList<Character> l3 = new LinkedList<Character>();

// adding an item
l2.add("One");
OR
l2.add(1, "Two"); // add(index, Object)

// changing an item
l2.set(0, "Wow") // changes the 0th element to "Wow"

// removing an item
l2.remove(0); // removes the 0th element

// removing every items
l2.clear();


```
