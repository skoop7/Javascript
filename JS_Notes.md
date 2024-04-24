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

OOPs
======================================
Object is basically collection of properties and methods

const user={}

this is called as object literal

```
const user={
    name:["John","Bob"],
    age:23,
    printDetails:function(){
        console.log("Details of users");
    },
    greet:function(){
        conole.log("Greetings!");
    }
}
methods->any function inside object
properties->it is key in object like name,age,etc.
```
You can access the object using . notation or []

user[name]="Alice new" or user.name="Alice new"

you can add new property

user.hobby=["Singing","Gaming"];

CLASS- 

Class is basically template from which multiple template can be created

INHERITANCE-

Child class will have all characteristics of its parent class + it have its own methods

```
class VIPCustomer extends customer{
    constructor(name,email,vipLevel){
        super(name,email), // to call constructor of parent class
        this.vipLevel=vipLevel;
    }

    updateVIPLevel(level){
        this.vipLevel=level;
    }
}
```
and you can call this using
```
const vipCustomer=new VIPCustomer("Alice","qwerty@gmail.com","Gold");
```
Child class can inherit all the methods of parent class


THIS Keyword
========================================

In function this keyword points to global object,

But in strict mode ,this keyword becomes undefined

If you are calling the function from object then value of this will be object

CALL,APPLY,BIND
========================================
These methods use for function sharing

```
const user={
    firstname:"Saurabh",
    lastname:"Kobarne",
    printfullname:function(){
        console.log(`Hi! My name is ${this.firstname} ${this.lastname}`);
    }
}
```
if i want to print the full name i can do it like this
```
user.printfullname();

```
and suppose there is second user 
```
const user2={
    firstname:"Mark",
    lastname:"Zukku",
}
```
I cant use printfullName method

so to do that we have call

```
user.printfullName.call(user2)
```
or you can make function generic

```
 printfullname:function(){
        console.log(`Hi! My name is ${this.firstname} ${this.lastname}`);
    }

and do it like this

printfullname.call(user);
printfullname.call(user2);
```
APPLY-
In apply we can pass parameter in array
```
printfullname.apply(user,["red","orange"])
```
Arrow function does not have their own this


PROTOTYPE
============================
First JS Engine checks for that value inside that object if its not there it checks for prototype and object property can shadow the protype property

All properties of object can be inherited to another object by using prototype

Lets take a example
```
const parent={
    a:10,
    b:20,
    sum:function(){
        console.log(this.a+this.b);
    }
}
const child={
    c:30,
    d:40,
    multiply:function(){
        console.log(this.c+this.d);
    }
}

so to inherit all the properties of parent object change the prototype of child to parent

child.__proto__=parent;
```
DOM(Document Object Model)
====================================
Its root node is Document

and its a tree like structure

To print the content we use InnerHTML

To add a class using JS we use classList.add("");

To insert any element before any element we use inssertbefore

but to use this you need to appendchild before it
```
parent.insertBefore=(newpara,existingpara);
```

To remove element we use 
```
.remove() method
```

ASYNCHRONOUS PROGRAMMING
=========================================
Instead of waiting for one task to complete before moving to the next one ,the program can start multiple tasks and come back to them later once they are done.

Asynchronous programming grants multitasking superpower to code.

JS is synchronous single threaded language

setTimeout is webAPI which executes after certain time

Whatever function taking time is sent to the browser instead of call stack ,and browser executes it behind the scene and once it completes it ,completed task get push to callback queue and then callback queue will check wheather call stack is empty or not and then it pushes it to call stack

Wahtever promises are there ,they are pput in microstack queue .it have higher priority than callback queue.

CALLBACK-

function passed as an argument to another function.

PROMISES-

Promises are mechanismfor handling asynchrous task without blocking the program execution flow.


JAVASCRIPT RUNTIME ENVIRONMENT-
=====================================

environment in which js runs/executed

it consist of mainly these things-

1.JS Engine- it is use to execute JS code having callstack and other things

2.Web API- Browser/NodeJS providing API like setTimeout ,localstorage,etc

3.callback Queue

4.Microtask Queue

5.Event loop

JS ENGINE
====================================

It is simple program written in low level language,which converts JS code into Machine Code.

Execution phses are like 

1.code

2.parse - It converts the code into tree like structure called as Abstract syntax tree 

3.compiled-

4.Execution

IS JS INTERPRETED LANGUAGE OR COMPILED LANGUAGE?
->IT DEPENDS ON HOW YOUR JS IS EXECUTING EG. V8 ENGINE USE JIT(Just in Time) compilation (combination of compiler and interpreter)


BROWSER OBJECT MODEL
======================================
There are several object given by browser such as Document buyt there are some addtional object such as alert,confirm,prompt

location is also object to redirct to the url


LOCAL STORAGE
======================
It is use to store object inside browser

length will give number of key value pairs present inside localstorage

SESSION STORAGE
==============================
Its key value pair does not reflect in another tab or another sesssion like localstorage

some methods are -

1.setItem

2.getItem

3.removeItem

4.clear - To clear all data from local or session storage

