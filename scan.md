```scan``` is used to perform parallelism in Chapel.It embodies a logic which performs a sequencial operation in parts 
and carries along the intermediate results.The syntax for ```scan``` is :
```Chapel
var varName = scan_operator scan iterator_expression
```
Let's understand through an example:
```Chapel
var array:[1..5] int = 1;
writeln(+ scan A);
```
