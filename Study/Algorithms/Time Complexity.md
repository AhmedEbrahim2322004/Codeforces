The time complexity of an algorithm means the amount of time taken by an algorithm to run as a function of the length of the input. Note that the time to run is a function of the length of the input and not the actual execution time of the machine on which the algorithm is running on.

### Big-O analysis

Let g and f be functions from the set of natural numbers to itself. The function f is said to be O(g) (read big-oh of g), if there is a constant **c > 0** and a natural number **n<sub>0</sub>** such that f(n) ≤ c . g(n) for all n ≥ n<sub>0</sub> .

## **Complexity classes:**

![[Time Complexity.jpeg]]
 
- **O(1)** The running time of a constant-time algorithm does not depend on the input size. A typical constant-time algorithm is a direct formula that calculates the answer.

- **O(log n)** A logarithmic algorithm often halves the input size at each step.  Ex (Binary Search)

- **O(n<sup>1/2</sup>)** A square root algorithm is slower than O(log n) but faster than O(n).

- **O(n)** A linear algorithm goes through the input a constant number of times. Ex (for loop)

- **O(n log n)** This time complexity often indicates that the algorithm sorts the input, because the time complexity of efficient sorting algorithms is O(n log n). Another possibility is that the algorithm uses a data structure where each operation takes O(log n) time.

- **O(n<sup>2</sup>)** A quadratic algorithm often contains two nested loops

- **O(n<sup>3</sup>)** A cubic algorithm often contains three nested loops.

- **O(2<sup>n</sup>)** This time complexity often indicates that the algorithm iterates through all subsets of the input elements.

- **O(n!)** This time complexity often indicates that the algorithm iterates through all permutations of the input elements.

## **Order of magnitude:**

A time complexity does not tell us the exact number of times the code is executed, but it only shows the order of magnitude.
**_Ex:_** (3n), (n+5) and (2n/2) the time complexity of each code is O(n).

**_NOTE_:** when we calculate the big O of the whole code we take the O with the highest time Complexity.
**_Ex_** (n+n2+2) the time complexity of the code is O(n<sup>2</sup>)

## **Estimating efficiency:**

![[Screenshot002.png]]

it is important to remember that a time complexity is only an estimate of efficiency, because it hides the constant factors.

**_Ex:_** an algorithm that runs in O(n) time may perform n/2 or 5n operations. This has an important effect on the actual running time of the algorithm.

**_NOTE:_** 1S is about 10<sup>6</sup> steps

## Recourses
- geeksforgeeks
- Competitive programming handbook

