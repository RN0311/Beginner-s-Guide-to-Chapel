## Variables 
Chapel supports several simple variable types and have somewhat different way of defining and initializing them. 
There are four basic types that one should know:

* **bool**
A boolean variable, which can hold values either true or false. But, has the default value false.

* **int**
Integer variable, whose default value is 0.We declare a ``` long ``` with int(64) as the type, but 64 bits has been the default int size starting with Chapel version 1.5. 
If you need it unsigned, declare it as type "uint". 

* **real**
Floating point variable, whose default value is 0.0 and is equivalent to a double in Java.

* **string**
Variable to hold strings of ascii characters; essentially identical to strings in Java, except that these are not objects, but primitives. 
String concatenation works the same in Chapel as it does in Java. <br >
The default value for string is ```"" (the empty string)```.
