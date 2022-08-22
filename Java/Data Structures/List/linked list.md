# Linked List

* Each data is called "Node"
* Due to the dynamicity and ease of insertions and deletions, they are preferred over the arrays or queues
* linear data structure where the elements are not stored in contiguous locations
* elements are linked using pointers and addresses
* Direct access possible
* Dynamic array, thus not have to assign size
* LinkedList is implemented using the doubly linked list data structure

```java
import java.util.LinkedList;

LinkedList<Integer> l1 = new LinkedList<Integer>();
LinkedList<String> l2 = new LinkedList<String>();
LinkedList<Character> l3 = new LinkedList<Character>();

// adding an item
l2.add("One");
OR
l2.add(1, "Two"); // add(index, Object)
l2.addFirst("First") // adds to the beginning of the list
l2.addLast(Last) // adds to the last of the list

// changing an item
l2.set(0, "Wow") // changes the 0th element to "Wow"

// removing an item
l2.remove(0); // removes the 0th element
l2.removeFirst(); // removes the first element
l2.removeLast(); // removes the last element

// removing every items
l2.clear();

// check if it contains
l2.contains("something");

// retrieves but does not remove, the head (first element) of this list
l2.element();

l2.getFirst(); // get first element
l2.getLast(); // get last element

l2.indexOf("something") // get the index of ___

l2.size(); // size of the list

// Iterating LinkedList
for (String str : l2){
      System.out.print(str + " ");
}


// and more... refer to 
// https://www.geeksforgeeks.org/linked-list-in-java/
```
