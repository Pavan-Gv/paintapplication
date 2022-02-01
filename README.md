# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html>
<body id="moon">
    <div id="boss">
<canvas id="myCanvas" width="800" height="800" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=2" id="box">circle</button>
<button onclick="shape=4" id="box">Square</button>
<button onclick="shape=6" id="box">Triangle</button>
<center>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(255, 72, 72);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(5, 28, 243);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(252, 255, 60);"></button>
</center>

<script>


const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height = 800;
canvas.width = 800;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let csize= 20;
let sqsize= 50;
let tsize=30;
let hand="black";
function change_color(element){
    hand=element.style.background;
}

    function showCoords(event)

    {
    var x = event.clientX-545;
    var y = yMax-event.clientY;
    var coords = "X coords: " + x + ", Y coords: " + y;
    document.getElementById("halo").innerHTML = coords;

        if (shape==2){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=hand;
            ctx.stroke();
        }

        if (shape==4){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=hand;
            ctx.stroke();
        }
        if (shape==6){
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.closePath();
            ctx.stroke();
        }

    
    
    }

</script>
<center><p id="halo" style="color: black;"></p></center>
<p style="color: black; font-family: sans-serif;" >Paint Application Developed by G V pavan kumar.</p>
<style>

#boss{
    text-align: center;
   
}
#myCanvas{
    background-color: white; 
    border: 1px solid #ffffff;
}
#box{
    background-color: white;
    color: black;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#Eren:hover{
    background-color:#ffffff36;
    transition: 0.5s;
}
#moon{
    background-color: rgb(10, 14, 245);


}
#Yagami{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#Yagami:hover{
    transition: 0.21s;
}
</style>
</body>
</html>
~~~

## OUTPUT:

![OUTPUT](/paint.png)

## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
