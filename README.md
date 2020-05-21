# learn_java_script
This is my java script learning project

## Insert java script output in HTML 
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
