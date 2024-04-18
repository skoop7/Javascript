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