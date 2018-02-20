Begin and CoBegin are various forms of asynchronous parallelization. 
###### Begin
Using **begin** statement on a process you create a different 
thread for each statement.
```Chapel
begin writeln("I'm awesome");
begin writeln("You too can be awesome!");
begin writeln("Everyone is awesome, you just need to change your perspective");
```

###### Cobegin
**cobegin** statements are different in that the calling code waits for the cobegin's block of parallelized code to finish before continuing
```Chapel
cobegin{
writeln("I'm awesome");
begin writeln("You too can be awesome!");
begin writeln("Everyone is awesome, you just need to change your perspective");
}
begin writeln("Lets' wait to be awesome!");
```
The **cobegin** example in above is almost equivalent to the begin example because all the **writeln** statements run 
asynchroniously, yet the main difference is that no code can run until the **cobegin** block has finished. Thus, the **writeln 
statement outside the cobegin block will always run last**.
