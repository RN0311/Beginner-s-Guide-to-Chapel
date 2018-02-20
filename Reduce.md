```Reduce``` operator combines a set of values to produce a single value.The syntax of reduce is : <br >
```Chapel 
var varName = reduce_operator reduce iterator_expression;
```
Valid **reduce_operators** are ``` +, maxloc , &, |, ^, &&, ||, min, max, minloc,``` and  ```* ```.

```Chapel
// For random number generation
use Random; 
config const seed = 2990;
var Array1: [1..20] int;

//Fill the array with random numbers.
fillRandom(Array1, seed, algorithm=RNG.NPB);
writeln("Array1 is: ");
writeln(Array1);

//To sum up all the values of Array1.
var sum = + reduce Array1;

//To find 1-norm of an array.
var one_norm = + reduce abs(Array1);
writeln("The 1-norm of Array1 is ", one_norm);
writeln();

//To find minimum value of array.
var minvalue = min reduce Array1;

//To find maximum value of array.
var maxvalue = max reduce Array1;

/* 
 To calculate Frobenius norm of array.
 
 The `Frobenius norm`_ is the square root of the sum over all elements
   of their respective squares.
*/ 

var frob_norm = sqrt(+ reduce Array1**2);
writeln("The Frobenius norm of Array1 is ", frob_norm);
   
```



