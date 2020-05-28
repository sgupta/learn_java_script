# learn_java_script
This is my java script learning project

## Insert java script output in HTML (https://www.w3schools.com/js/js_intro.asp)
use "document.getElementById("<id>").innerHTML"  inside HTML page to display output of java script in location where id match in HTML tags.
  Example
  ```
  <!DOCTYPE html>
      <html>
        <head>
          <title>First java script lesson</title>
        </head>
        <body>
          <h1 id="demo"></h1>
          <p>Contents above are being added from javascript<p>
          <script>
            document.getElementById("demo").innerHTML = "I am output from JavaScript"
          </script>
         </body> 
      </html>
```
  
  ## Use java script to change image source by press of button
  In this example, use button element to call java script to change image source inside image tag
  
  ```
  <!DOCTYPE html>
<html>
    <head>
        <title>First java script lesson</title>
    </head>
    <body>
          <h1>ON and OFF bulb on press of button</h1>
          <button onclick="document.getElementById('myimage').src='images/pic_bulbon.gif'">Turn ON</button>
          <img id="myimage" src="images/pic_bulbon.gif">
          <button onclick="document.getElementById('myimage').src='images/pic_bulboff.gif'">Turn OFF</button>
    </body>
</html>

```
  
  ## Java script to change style (CSS)
  
  ```
  <!DOCTYPE html>
<html>
    <head>
        <title>Third java script lesson</title>
        <style>
            p {
                font-size: 20px;
                text-decoration-style: wavy;
            }
        </style>
    </head>
    <body>
          <h1>Change font size on press of button</h1>
          <button onclick="document.getElementById('mytext').style.fontSize = '35px'">Font size 35</button>
        <p id="mytext">This is my text</p>
          <button onclick="document.getElementById('mytext').style.fontSize = '55px'">Font size 55</button>
        <script>
            let fsize = "45px";
            document.getElementById('mytext').style.fontSize = fsize;
        </script>
    </body>
</html>
 ```
## Java script function
Java script function is block of code which can be called on event like press on button. Example below

```
<!DOCTYPE html>
<html>
    <head>
        <title>Third java script lesson</title>
        <style>
            p {
                font-size: 20px;
                text-decoration-style: wavy;
            }
        </style>
         <script>
            function setFont45() {
            let fsize = "45px";
            document.getElementById('mytext').style.fontSize = fsize;
            }
            function setFont35() {
            let fsize = "35px";
            document.getElementById('mytext').style.fontSize = fsize;
            }
        </script>
    </head>
    <body>
          <h1>Change font size on press of button</h1>
          <button onclick="setFont35()">Font size 35</button>
          <p id="mytext">This is my text</p>
          <button onclick="setFont45()">Font size 45</button>
       
    </body>
</html>
```
## External java script 
use ```<script src="js/setfontsize.js"></script>``` to load script from "js" directory inside HTML page.
use ```<script src="https://www.w3schools.com/js/myScript1.js"></script>``` to load script from url inside HTML.

## Java script output 
There are few possibilities to send output from from java script. Like in some examples above we using HTML element to send java script output 

###  HTML element, using innerHTML

```
<script>
   document.getElementById("demo").innerHTML = "I am output from JavaScript"
</script>
```
### HTML output using document.write()
This is use for testing purpose. Using document.write() after an HTML document is loaded, will delete all existing HTML:
```
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>
<p>My first paragraph.</p>

<button type="button" onclick="document.write(5 + 6)">Try it</button>

</body>
</html>
```
###  Alert box, using window.alert()
Pop an alert box 
```
<script>
window.alert(5 + 6);
</script>
```
### Browser console, using console.log()
Also used for debugging as this output do not display to use in browser but visible in debug mode 
```
<script>
console.log(5 + 6);
</script>
```
### Print in java script 
JavaScript does not have any print object or print methods.You cannot access output devices from JavaScript.The only exception is that you can call the window.print() method in the browser to print the content of the current window.
This used to provide users option to print page.
```
<!DOCTYPE html>
<html>
<body>

<button onclick="window.print()">Print this page</button>

</body>
</html>>
```
### Arithmetic operations 
Most of Arithmetic operations are similar to other languages 
```
<!DOCTYPE html>
<html>
    <head>
        <title>Arithmetic operations</title>
        <style>
            p {
                font-size: 20px;
                text-decoration-style: wavy;
            }
        </style>
         <script src="js/setfontsize.js"> 
        </script>
    </head>
    <body>
          <h2>Print x + y using java script</h2>
        <p> x = 10 , y = 20; 
        <p>Result for x + y <p id="e1"></p>
        <p>Result for x += y <p id="e2"></p>
        <p>Result for x =+ y <p id="e3"></p>
        <p>Result for x <<= y <p id="e4"></p>
           <script>
                var x = 10;
                var y = 20;
                var e1 = x + y;
                var e2 = x += y;
                var e3 = x =+ y;
                var e4 = x <<= y;
                document.getElementById("e1").innerHTML = e1;
                document.getElementById("e2").innerHTML = e2;
                document.getElementById("e3").innerHTML = e3;
               document.getElementById("e4").innerHTML = e4;
            </script>
    </body>
</html>
```
## Javascript Objects
Objects are variables too. But objects can contain many values.This of objects are actual objects which has attributes and actions. To understand better , lets assume you building a game with many players. Player can be object with attributes like "firstName" and "lastName" ,"age" and "city" . Object can also have functions like print fullname of player , print welcome message for player. 

```
<script>
            var player = {
                firstName:"Peter",
                lastName:"England",
                age:32,
                city:"Atlanta",
                printName:function() {
                    return this.firstName + " " + this.lastName;
                },
                printWelcomeMessage:function() {
                    return "Welcome to game " + this.firstName + " " + this.lastName + " from " + player.city;
                }
            };
            document.getElementById("fn").innerHTML = player.firstName;
            document.getElementById("ct").innerHTML = player.city;
            document.getElementById("pn").innerHTML = player.printName();
            document.getElementById("welcome").innerHTML = player.printWelcomeMessage();
        </script>
 ```
## Javascript events
Event can be something the browser does, or something a user does.Often, when events happen, you may want to do something.JavaScript lets you execute code when events are detected.HTML allows event handler attributes, with JavaScript code, to be added to HTML elements.
```
<element event='some JavaScript'>
#In the following example, an onclick attribute (with code), is added to a <button> element:
<!DOCTYPE html>
<html>
<body>

<button onclick="document.getElementById('demo').innerHTML=Date()">The time is?</button>

<p id="demo"></p>

</body>
</html>
```
|Event|	Description|
--------------------
|onchange|	An HTML element has been changed|
|onclick|	The user clicks an HTML element|
|onmouseover|	The user moves the mouse over an HTML element|
|onmouseout|	The user moves the mouse away from an HTML element|
|onkeydown|	The user pushes a keyboard key|
|onload|	The browser has finished loading the page|
