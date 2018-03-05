## Factorial

```Chapel
proc factorial(n : int) : int {
  if n <= 1 then return 1;
  return n * factorial(n-1);
}
```
```Chapel
writeln(factorial(6)) 
```
