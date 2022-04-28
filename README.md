# JS-notes

Async JS

1st Phase
when a browser made a request to the
server for a particular page the server
would find the html file stored on its
hard disk and set it back to the browser

2nd Phase
not long after that server started
pre-processing the html before it was
sent to the client every time a browser
would request a page based on the user's
cookies or authentication headers the
server would generate the html on the
fly for that specific user this allowed
but this process meant
that every change in a page's content
required a full page refresh

3rd Phase
ajax allowed browsers to send and receive data from
the server without needing to reload the page 

callback f -> function passed as arguments in functions
callback f uses:
1. transforming one value to another
const mapCallback= i => i+5
[1,2,3].map(mapCallback)
2. delaying execution of a function until a particular time (until we receive data from an external API instead of delaying execution until we click the button)
const onClickCallback = () => c.log("Button is click")
<button onClick={onClickCallback}>BUTTON</button>

Call back hell or pyramid of doom forces you out of natural way of thinking with each level of nesting
![Screenshot (27)](https://user-images.githubusercontent.com/67150257/155607371-c8eaad17-5e6a-4bed-9626-ba84ad507267.png)

Callbacks causes inversion of control
the notion of having code under your control in one part of the program, 
then handing control over to a callback in another part of the program(so this 3rd party library could break how they interact with your callback).
Example:
You want to reserve a table at a resturant:
If you give your phone no for them to ping you (inversion of control => they could send adds)
If they give you a buzzer (when you receive the buzzer(default or pending state), when table is ready, buzzer green(fullfilled) and rest closed(rejected, something goes wrong))
pending, fullfilled, rejected are status of async request

Promise is an object, method then handles resolve, catch handles reject
Promise takes 2 arguments resolve and reject
Biggest problem with chaining is getting state down the chain, so async await


Funtional Prog in JS
Input returning output

The main thing about FP is to use pure functions 
Pure functions avoid side effects
data st, logic, iteration all are independent

Using higher order functions
Taking functions as IPs or returning functions as OPs

Using map, reduce, filter
Immutability- not susseptable to change, fixed
leads to the creation of new data structures (inc space and time complexxxx)

Persistent data structures for for efficient immutability
Uses structural sharing (lessens space and time complexxx) - tree struct - leaf node shared 

filter - filters out things according to conditions

single threaded -> js can run one piece of code at a time
non blocking -> , async conc lang
contains call-(ds which records where in the program we are, pushes something into the stack when function call happens, and pops something out of the stack when returned)
, event loop and other apis

blocking means things which are slow on the stack(image, network request)
sync - one thing at a time which does not give nice fluid UIs for users since at that the time the call stack has things on it and the browser is stuck, it cant do anything else

for this sync we use  cbs, where we run some code give it a cb which we run it later

not defined- nowhere in program Reference Error
undefined- initialiazed and present in the memory but its value hasnt been read yet
fat arrow functions arent given space in the memory while normal fun are, to check this  call them before they are initialized

TDZ(zone in scope where let and const aren't declared.), Hoisting

The let and const variables exist in the TDZ from the start of their enclosing scope until they are declared.
Why TDZ?
JS moves all your variable declarations to the top of their scope (Hoisting)

var gets undefined initialized while hoisting.
let and const also get hoisted, but don't get set to undefined. So a TDZ occurs because let and const aren't properly hoisted.

NCO ??
If x is either null or undefined then only result will be y.
If x is not null or undefined then the result will be x.

OR ||
returns first truthy value

AND &&
returns first falsy value else truthy value

OPTIONAL CHANING
No chaining with AND or OR operators unless a parenthesis is provided to explicitly indicate precedence
If we want some of them to be optional, then we’ll need to replace more . with ?.
?. immediately stops (“short-circuits”) the evaluation if the left part doesn’t exist.
obj?.prop – returns obj.prop if obj exists, otherwise undefined.
obj?.[prop] – returns obj[prop] if obj exists, otherwise undefined.
obj.method?.() – calls obj.method() if obj.method exists, otherwise returns undefined.

A polyfill is a piece of code (or plugin) that provides the technology that you, the developer, expect the browser to provide natively. 

tc39 is a committe deciding how ecmascript should work

A shim is any piece of code that performs interception of an API call and provides a layer of abstraction. It isn't necessarily restricted to a web application or HTML5/CSS3.

A polyfill is a type of shim that retrofits legacy browsers with modern HTML5/CSS3 features usually using Javascript or Flash.

//browser code for O/P

Closures
// 1) Closures are a property of JavaScript functions
// 2) Call function in different scope than where function was original defined
// 3) Closures helps preserves values



https://onecompiler.com/javascript/3xzdjeyju

DEEP-SHALLOW COPY
https://onecompiler.com/javascript/3xz87v8ae

CALL,BIND,APPLY
https://onecompiler.com/javascript/3xzdpccx6

ARROW FUNCTIONS
https://onecompiler.com/javascript/3xzeehg33

Factory Functions
https://onecompiler.com/javascript/3xzn2hrc9

Settimeout
https://onecompiler.com/javascript/3xzv939g3

Currying
https://onecompiler.com/javascript/3xznzm6bn

Use strict
https://onecompiler.com/javascript/3y2cpxrpg

A constructor enables you to provide any custom initialization that must be done before any other methods can be called on an instantiated object.

Creating Objects
https://onecompiler.com/javascript/3y2cugcj2 

proto is a property of every object that points to the parent object that it is inherting from whearas prototype is a property on constructor function that has all the stuffs that will be inherited by its instance

Prototypal inheritence
https://onecompiler.com/javascript/3y2d58wp2

Primitives are assigned by values while objects are assigned by reference
https://onecompiler.com/javascript/3y2dhcmja


Promises
https://onecompiler.com/javascript/3y2dr3rh8





