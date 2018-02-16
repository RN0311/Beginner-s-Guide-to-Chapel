In **Chapel**, *for* loops have the following syntax: <br >
###### For
```Chapel 
for index-expression in iterable-expression {
         //follow-up statements
}
```
```Chapel 
for i in {1..5}{
    write(i," ");
}
```
**Do-While** and **While** share the same syntax:<br >
###### While
```Chapel
while(condition){
  //do some work
}
```
```Chapel
var i = 5;
var t:int;
while(i>t){
  writeln(t,' ');
  t = t + 1;
}
```
###### Do-While
```Chapel
do{
  // do some work
}while(condition);
```
```Chapel
var j = 0;
do{
	writeln(j,'');
	j = j + 1;
}while(j <= 5);
```
