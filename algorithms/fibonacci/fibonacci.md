## Fibonacci Series
> A series of numbers in which each number is the sum of two preceding numbers.

Code
```Chapel
iter fibonacci(n: int) 
{
  var (now, new) = (0, 1);
  for 1..n 
  {
    yield now;
    (now, new) = (new, now + new);
  }
}
write("Fibonacci series: ");

for num in fibonacci(10) do
  write(num, ", ");
```
