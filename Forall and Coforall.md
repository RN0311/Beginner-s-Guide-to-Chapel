## Parallelism in Chapel
* Data Parallelism
  * Parallelism is driven by collection of data
    * data aggregates(arrays)
    * sets of indices(ranges, domains)
    * other user-defined collections.
    * eg. ``` for all elements in array A ```
* Task Parallelism
   * Parallelism is expressed using distinct tasks
   * eg. ``` create a task to do foo() while another does bar() ```
  
### Forall 
Forall loops are a simple and easy way to run similar tasks in parallel using a for loop. When a forall loop runs, it creates a thread for 
each core of the processor.After the threads have finished they are joined together to form the result. 
```Chapel
var sum : int = 0;
forall i in 1..200000 {
sum += i; //race condition!
}
writeln(sum);
```
### Coforall
In a coforall loop, a new thread is created at each iteration through the loop. This is useful in cases in which each iteration
has a substantial amount of work,and the number of tasks should be equal to the number of iterations.
```Chapel
config const numTasks = here.numCores;
coforall tid in 1..numTasks {
writeln("Hello, world"," from task ",tid," of ",numTasks,"!");
}
```

  
