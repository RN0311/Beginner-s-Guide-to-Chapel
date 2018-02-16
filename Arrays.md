## Arrays
```Chapel
//Initialize 1D array.
var Array1: [1..20] int;
var Array2: [{1..20}] int;

//To access 1D array.
for i in 1..20 do
  Array1[i] = -i;
writeln(Array1);

//Initialize 2D array.
var realDomain: domain(2) = {1..10,1..15};
var realArray: [realDomain] real;
var Array3 = [1..10,1..15] real;

//To access 2D array.
for i in 1..10 {
  for j in realDomain.dim(2) {   // Only use the 2nd dimension of the domain
    realArray[i,j] = i + j;  
  }
}

```
