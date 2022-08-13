# Big O Notation

__Big O Notation:__ 
* To analize efficiency of the algorithms as its input approaches to infinity.
* Describes the complexity of your code using algebraic terms

## O(1): Constant Time Complexity
* Will always take same amount of time to be executed no matter the size of an input.
* Has Least complexity

```java
// Example 1: Accessing an array
int[] array = {1,2,3,4,5};
array[2]; // => 3

// Example 2: adding an item to an array
 array[n++] = 6;
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
* Time it takes to run the algorithm is proportional to the logarithm of the input size n

```java
// Binary Search

```

## O(n^2): Quadratic time complexity
 * Time to execution it is proportional to the square of the input size
 * Simple example is to check if there are any duplicates in a deck of cards
 ```java
 for(int i = 0; i < length; i++){
    // has O(n) time complexity
    for(int j = 0; j < length; j++){
        // has O(n^2) time complexity
    }
 }
 ```
 __Types of O(n^2)__
* Selection Sort: iterates through the list to ensure every element at index i is the ith smallest/largest element of the list
* Bublle Sort: 

## O(n log n)


## Big O Notation Graph
![Big O Notation Graph](https://user-images.githubusercontent.com/93812258/184478719-733aa1ac-7b2b-47fa-90bd-a076898f8b65.png)
\(From https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)

## Data Structure Operations
![Data Structure Operations](https://user-images.githubusercontent.com/93812258/184476914-b0c1a7c6-1584-4795-a7a3-0b2ac71fdfdd.png)
(From https://www.bigocheatsheet.com/)
