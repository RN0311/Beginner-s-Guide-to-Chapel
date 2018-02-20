## Procedures
Procedures are Chapel's functions/methods. They are declared with keyword ```proc``` followed by the name of procedure.
```Chapel
proc say_hello(){
  var name: string = getName();
  writeln("Hey!, ",name,"!");
} 
```
For example, in Python we use ```def``` keyword for functions while in Chapel we use ```proc```. 
###### Python
```Python
def abs(x):
    if x < 0:
        return -x
    else:
        return x
```
###### Chapel

```Chapel
proc abs(x):
    if x < 0:
        return -x
    else:
        return x
