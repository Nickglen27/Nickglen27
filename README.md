<!DOCTYPE html>
<html>

<h1><p ondblclick="myFunction()">1.)Double-click HERE</p></h1>
<p id="a"></p>
<h3>2.)Press ArrowUp</h3>
<style>
        .h1 {
            width: 100%;
            height: 600px;
            background-size: cover;// css style This is for the red background
        }
    </style>
    <body>
    <div class="h1"><h4>3.)Move the mouse HERE</h4></div>

  
    <script>//Double-click
      function myFunction() {
  document.getElementById("a").innerHTML = "<h2>Welcome User</h2>";
}//a declaration unless used in the context of an expression at which point it becomes one and the document.geElementById i called "a" for the id name.


      //Mouse move
        var div =
            document.querySelector(".h1");//it's returns the first Element within the document that matches the specified selector, or group of selectors which is the "h1"
  
        div.addEventListener(//this method attaches an event handler to an element
            "mousemove", function (e) {//when the mouse is moving under the class"h1" the background will attached
                x = e.offsetX;
                y = e.offsetY;
                div.style.backgroundColor
                    = red;//and my background color
            });


      //Key up
        document.addEventListener('keyup', (event) => {//keyup event is sent to an element when the user releases a key on the keyboard.
    var name = event.key;
    if (name === 'ArrowUp') {
      alert('You had pressed a key');//If the ArrowUp key is pressed without any combination, the code listens to the keyup event and creates an alert
    } 
  }, false);
    </script>
</body>
</html>
