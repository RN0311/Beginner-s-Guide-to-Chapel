## Chapel's struct/object type:
* Contain procedure & iterator definitions (methods)
* Records: value-based (e.g., assignment copies fields)
* Classes: reference-based (e.g., assignment aliases object)
* Record:Class :: Java class 
###### Records 
```chapel
record circle{
 var r: real;
 proc circumference(){
      return 2 * 3.14 * r;
 }
}


var c1,c2:circle;
c1 = new circle(12.0);
c2 = c1;
c2.r = 10;
writeln("The circumference of circle is ",c1.circumference()); //75.36
writeln("The circumference of circle is ",c2.circumference()); //62.8
```
###### Classes
```Chapel
class circle {
 var radius: real;
 def circumference() {
   return 2*3.14*radius;
 }
}


var c1, c2: circle;
c1 = new c1(radius=1.0);
c2 = c1; // aliases c1’s circle
c1.radius = 5.0;
writeln(c2.radius); //5.0
```
