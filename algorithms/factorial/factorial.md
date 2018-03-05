## Fibonacci Series

```Chapel
proc fibonacci(n : int) : int {
  if n <= 1 then return n;
  return fibonacci(n-1) + fibonacci(n-2);
}
```
```Chapel
writeln(fibonacci(6)) //8
```