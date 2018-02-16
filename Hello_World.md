## "Hello World" in Chapel

* Fast prototyping
```Chapel 
writeln("Hello, world!");
```
* Production Grade
```Chapel
module Hello
{
  config const variable = "world"; 
  proc main(){
    writeln("Hello,",variable,"!");
  }
}
```
* Now, compile it:  ``` chpl -o hello <directory-name>/<-name-of-file.chpl> ```
* Run it: ```./hello```
