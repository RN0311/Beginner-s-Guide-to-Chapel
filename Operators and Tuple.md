## Operators
###### Math Operators
```Chapel 
* var r: int, first_num = 11, second_num = 22;
* r = first_num + second_num;  // Addition 
* r = first_num * second_num;  // Multiplication
* r = first_num - second_num;  // Subtraction
* r = first_num / second_num;  // Division
* r = first_num ** second_num; // Exponentiation
* r = first_num % second_num;  // Remainder(Modulo)
```
###### Logical Operators
```Chapel
* var r: bool, first_bool = false, second_bool = true;
* r = first_bool && second_bool; // Logical and
* r = first_bool || second_bool; // Logical or
* r = !second_bool;            // Logical negation
```

###### Relational Operators
```Chapel
var a = 40
var r: int, first_num = 30, second_num = 50;
r = first_num > second_num;           // Greater-than
r = first_num >= second_num;          // Greater-than-or-equal-to
r = first_num < a && a <= second_num; // Less-than, and, less-than-or-equal-to
r = first_num != second_num;          // Not-equal-to
r = first_num == second_num;          // Equal-to
```

###### Swap Operators
```Chapel
* var first_num = 11;
* var second_num = 22;
* var i = first_num;
* var j = second_num;
* i <=> j; // Swap the values of first_num and second_num
* writeln((i == second_num) && (j == first_num));
```

## Tuples
Tuples can be of same type or different type.
```Chapel
* var tuple1 = (100,100.05,100+0.05i);
* var tuple2 = (100,200);
// To access same tuple using square brackets or paranthesis
* writeln("(",tuple2[1],",",tuple2[2],")");
// or
* writeln("(",tuple1[1],",",tuple1[2],")");
