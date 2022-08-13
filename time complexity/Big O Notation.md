# Big O Notation

__Big O Notation:__ To analize efficiency of the algorithms as its input approaches to infinity.

## O(1): Constant Time Complexity
* Will always take same amount of time to be executed no matter the size of an input.

```java
// Example 1: Accessing an array
int[] array = {1,2,3,4,5};
array[2]; // => 3
```

## O(n): Linear time complexity
* Time needed to execute the algorithm is directly proportional to the input size n
* Simple example is reading a book with n pages

```java
// Linear Search
int[] array = {1,2,3,4,5};

for(int i = 0; i < array.length; i++){
  System.out.println(array[i]);
}
```


## O(log n): Logarithmic time complexity
## O(n^2): Quadratic time complexity
 
