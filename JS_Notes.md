Always use const for declaring arrays and object

Avoid using var as it override value from anywhere

```
There are 8 datatypes-
1.Number
2.String
3.Boolean
4.null
5.undefined
6.BigInt
7.Symbol -to store unique values
8.Object

typeof - to check datatype of variable
```
```
Type of operators-
1.Arithmatic
2.Comparison
3.Logical 
4.Assignment
5.Conditional
6.Type
```

```
Switch statment syntx is like

Switch(dayNumber){
    case 0:
    day="Monday";
    break;
    case 1:
    day="Tuesday";
    break;
    default:
    day="Please provide correct day number";
}
```
whatever will be the dayNumber value it will execute according to that

To loop through object we can use for in loop
```
user={Harry:56,Akash:57,Suraj:78}

for(key in user){
    console.log(user[key]);
}
```
To loop through array you can use for of loop
```
const fruits=["apple","mango","guava"];

for(fruit of fruits){
    console.log(fruit);
}
```
EXECUTION CONTEXT-

Everything in javascript in an environment called as execution context

Two things happens inside it-

1.Memory allocation

2.Code Execution

Able to access variable before declaring it called as Hoisting

In function expression/Arrow function hoisting is not done
Hoisting can be done only in normal function

```
You can use String quote inside quote by escape sequence

const string="hello my name is \"Saurabh \" and I am a good web developer

to use quote inside quote you can use single quote and double quote
```
You can create String two ways
```
1.Using object i.e. by using new keyword

2.let string1="Helllo World"
```
If you compare two objects it will always give False
```
If you want to compare the value of objects then use valueof() method

let color1= new String("red");
let color2= new String("red");

console.log(color1.valueOf()===color2.valueOf());
```
STRINGS-

Methods of strings are as follows:
```
replace('Hi','Hello') // replace only first one
replaceAll('Hi','Hello'); // replace all strings
split(" "); // it will return array
repeat(2); // it will repeat text two times
trim(); //it will remove extra white space;
trimStart(); //it will only trim start part of strim
trimEnd(); //it will trim from end part
concat(); //it will concatinate 2 strings
```
some other methods are:
```
charAt(index); // it will return character

charCodeAt(6); //It return ASCII value;

at(-1); //It is same as charAt but you can use -ve indexing here it will start from end due to negative indexing value

text[2]; //you can access character like this but only read cannot modify

slice(start,end); //To extract substring from given index to ending index but ending index not included only diffrence between slice and substring is slice consider -ve index

substring(start,end); //it will not consider -ve index.remaining same as slice;

toLowerCase() //to convert string into lowercase

toUpperCase() // to convert string into uppercase
```
ES6-

var is global scope variables

while let is a lock scope variable

let variable cannot be redeclare

const is also a block scope variable. Variable with const canno be redeclare and reinitialise.


TEMPORAL DEAD ZONE-

let and const can only be used after initialization i.e. they cannot be hoisted

let and const stay in temporal dead zone till the value is initialise to them

FUNCTION-
As compare to global variable local variable have higher priority

```
INSIDE STUFF:

In GEC(Global Execution Context) two areas are there

1.Memory Allocation

2.Code Execution

lets take example

var z=10;
x();
y();
console.log(z);
function x(){
    var z=20;
    console.log(z);
}
function y(){
    var z=30;
    console.log(z);
}

in this firstly z gets memeory allocation having value undefined later function x(){} will have memory allocation
later function y(){} will have memory allocation

after memory allocation completion code execution get started

firstly var z will have value 10 instead of undefined and it will reflect in memory allocation later we x() function execution so local execution context will be created inside code execution block and inside callstack on top of the GEC(which is at bootom of call stack) x will be pushed
and same process of memory allocation and code execution is happen in function x local context and when its done x will be pop out of the call stack. same for y.
```
PASSING FUNCTION INSIDE FUNCTION or RETURN FUNCTION FROM FUNCTION CALLED AS FIRST CLASS FUNCTIONS.AND IT TREATED LIKE A VARIABLE.

IIFE(Immediately invoked function expression) are also called as self invoking function.This is use for data privacy


If you declare any variable inside function you can access inside function and another functions inside it(Inner functions) but you cannot access outside the function.
but variable declare outside the function can be access because of scope chain due to lexical environment

Parent variable can be use by children but children variable can not be use by parent

Var overshadows the other var variable as it is in global cope but let and const dont as they are in block scope

A function along with its lexical environment called as closure

ARRAY-
```
methods of Array

1.length (it start from 1); //last index will be length-1
2.toString(); //to convert array into single string
3.join("%"); //it is similar to tostring but it join all the strings using % here
4.at
5.push/pop //to add or remove the element from end of an array
push method return new length while pop method return pop element
6.Shift (remove from start of an array); //it return shifted element.
7.unshift (add from start of an array); //return new length of an array
8.delete arr[1]-delete the item from array but maintain empty space where element is deleted
9.splice(start index,number of elements to delete);// it modify original array and it does not keep empty spaces

const a= [1,2,3,4,5];
a.splice(2,1) - 1,2,4,5
a.splice(2,1,4,6,7,9)- 1,2,4,6,7,9,4,5 // basically it will delete that position and replace it with these numbers

10.slice(start index,end index (not included)) - it will return new array

11.tosplice()-same as splice but return new array
```
we have other methods also

```
1.concat-arr1.concat(arr2); it will concat arr1 and arr2 or you can do arr1.concat(arr2,arr3);or arr1.concat("6");
2.flat-
    const a=[[1,2],[3,4],[5,6]];
    a.flat();//[1,2,3,4,5,6];-this will return new array
3.indexof()-
    const colors=["green","orange","red"];
    colors.indexof("red");//2
    if value is not present then it will return -1
4.lastindexof()-
    const colors=["red","orange","green","red"];
    colors.lastindexof("red");//3
5.includes()-
    it will return boolean value where item it is present or not
```
SORTING-

There are some methods of sorting some of them as follows
```
1.sort()-it will sort the original array
2.toSorted()-it will sort the array and new array gets created and orginal array dont affect
3.reverse()-it will reverse the elemets of my array it dont sort and itmodify original content
4.toReverse()-its same as reverse but not modify original array
```
In case of numerical sorting order is not correct as it sort alphabetically
to sort numbers we should use compare function

```
arr.sort(function(a,b){return a-b});
negative keep a before b
```
to get minimum and maximum value we have 2 functions called as Math.min and Math.max respectively.

we mostly use for of loop for array looping

HIGHER ORDER FUNCTION-
It is a function which take function as parameter  or return function

function y(x){
    x();
}
x->x is a callback function
y-> y is a higher order function


MAP- 
it will change content o array but create new array

```
const arr=[1,2,3,4,5];

function square(x){
    return x*x;
}
const squaredArray=arr.map(square);
```
FILTER- Filter out elements based on condition

EVERY-
it returns TRUE if all elements satisfies the condition

SOME-Even if single element satisfies the condition it returns true

FIND- It will return the first element which satisfies the condition

FINDLAST-It will return the last element which satisfies the condition

FINDINDEX-It will return the index 

FINDLASTINDEX- It will return last index

