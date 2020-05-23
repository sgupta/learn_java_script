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
