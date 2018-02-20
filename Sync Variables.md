*Synchronization variables have a logical state associated with the value. 
The state of the variable is either full or empty. <br >
Chapel supports two types of synchronization : ```sync``` and ```single```.Both of these types, behave similarly except that a single 
variable may only be written once.*

To prevent race conditions on variable updates, we use ```sync``` variables.When a sync variable is full it will stop any other thread to use it 
until it is turned empty.

```Chapel
var sum : sync int = 0;
forall i in 1..20000{
  sum += i;
}
writeln(sum);
```
The above example, shows that a sync variable is set to full when it is given a value and it is set to empty whenever 
it is assigned to another sync variable.
<br >
<br >
Also, sync variables can be used as a lock. Let's see how : 
```Chapel
var lock: sync bool; //the sync variable
var sum: int = 0;
forall i in 1..20000{
  lock = true; 
  sum += i;
  var unlock = lock; 
}
writeln(sum);
```
Now, let's see potential of ```sync``` that how it prevents race condition.When sync is applied to a block of code, it will join together 
all the **begin** statements started within that block of code. 
```Chapel
sync {
begin writeln("I'm awesome");
begin writeln("You too can be awesome!");
begin writeln("Everyone is awesome, you just need to change your perspective");
}
begin writeln("Lets' wait to be awesome!");
```
