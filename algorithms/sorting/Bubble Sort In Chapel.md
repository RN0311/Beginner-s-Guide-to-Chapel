## Bubble Sort
> It is the simplest sorting algorithm which works by repeatedly swapping the adjacent elements if they are in the wrong order.

###### Bubble Sort

```Chapel
writeln("Input size of array");

//total number of elements
var num_of_elements = read(int); 

var arraylist: [0..num_of_elements-1] ; 

writeln("Input elements of array");
for i in 0..(num_of_elements - 1){
    arraylist[i] = read(int);
}


//sorts array using bubble sort
var temp = 0;
for j in 0..(num_of_elements - 2){
    for k in 0..(num_of_elements - j){
        if arraylist[k]>arraylist[k+1] {
            temp=arraylist[k];
            arraylist[k]=arraylist[k+1];
            arraylist[k+1]=temp;
        }
    }
}


//Print sorted array
for i in 0..num_of_elements-1{
    writeln(arraylist[i]);
}
```
