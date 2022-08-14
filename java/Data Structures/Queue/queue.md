# Queue

* FIFO (First In First Out)
* Used in BFS

```java
import java.util.Queue
import java.util.LinkedList;

// in java, we need to use LinkedList to declare a Queue
Queue<Integer> queue = new LinkedList<>();
Queue<String> queue2 = new LinkedList<>();

// adding items
queue.add(1);
OR
queue.offer(1);

// removing items
queue.remove() // removes the first element
OR
queue.poll(); // removes the first element; if empty, null

// remove everything
queue.clear();

// Get the first item
queue.element(); // Retrieves, but does not remove, the head of this queue
OR
queue.peek(); // Retrieves and removes the head of this queue, or returns null if this queue is empty.
```
