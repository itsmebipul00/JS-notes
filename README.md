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
-
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

Using higher order functions
Taking functions as IPs or returning functions as OPs

Using map, reduce, filter
Immutability- not susseptable to change, fixed
leads to the creation of new data structures (inc space and time complexxxx)

Persistent data structures for for efficient immutability
Uses structural sharing (lessens space and time complexxx) - tree struct - leaf node shared 


