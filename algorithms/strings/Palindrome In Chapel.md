## Palindrome
> A string is palindrome if the reverse of that string is same as original string. For example, 
“dad” is palindrome, but “daddy” is not a palindrome.

```Chapel
//read input string.
var str : string = stdin.read(string);

//n represents length of string.
var n : int = str.length;

//Declares a sync variable palindrome of type bool and initialzes it to true.
var palindrome : sync bool = true;  				


forall i in 1..n/2
{
  if(str.this(i) != str.this(n-i+1))
  {
  	//state of sync variable is empty
	palindrome;			
	//state of sync variable is full 
	palindrome = false;			         	
   }
}


var flag : bool = palindrome.readFE();
if flag == true then
	writeln(str," is palindrome");
else
	writeln(str," is not a palindrome");
```
  
