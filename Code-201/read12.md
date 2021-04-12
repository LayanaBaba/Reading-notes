**EASILY CREATE STUNNING ANIMATED CHARTS WITH CHART.JS**

Charts are better for showing data than tables. You can make a charts using Charts.js. 

* SETTING Up: 
We need to download Chart.js, then create a new HTML page and import the script.

* DRAWING A LINE CHART:
1- You must add this to the body of our HTML page:
< canvas id="buyers" width="600" height="400"></ canvas>

2- You must add this to the footer:
< script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</ script>

3- Inside the same script tags we need to create our data:
var buyerData = {
    labels : ["January","February","March","April","May","June"],
    datasets : [
        {
            fillColor : "rgba(172,194,132,0.4)",
            strokeColor : "#ACC26D",
            pointColor : "#fff",
            pointStrokeColor : "#9DB86D",
            data : [203,156,99,251,305,247]
        }
    ]
}


THE < canvas> ELEMENT
This element has two attributes, width and height. Providing fallback content is very straightforward: just insert the alternate content inside the < canvas> element. The < canvas> element requires the closing tag (</ canvas>). 


* DRAWING SHAPES WITH CANVAS
THE GRID:
The origin of the grid is positioned in the top left corner at coordinate (0,0). 

* Drawing rectangles:
There are three functions that draw rectangles on the canvas:
1- Draws a filled rectangle:
fillRect(x, y, width, height).
2- Draws a rectangular outline:
strokeRect(x, y, width, height).
3- Clears the specified rectangular area, making it fully transparent:
clearRect(x, y, width, height). 

* Drawing paths:
To make shapes using paths, we take some extra steps:
1- First, you create the path.
2- Then you use drawing commands to draw into the path.
3- Once the path has been created, you can stroke or fill the path to render it.
 
The functions used to perform these steps:
1- Creates a new path:
beginPath().
2- Methods to set different paths for objects:
Path methods().
3- Adds a straight line to the path, going to the start of the current sub-path:
closePath().
4- Draws the shape by stroking its outline:
stroke().
5- Draws a solid shape by filling the path's content area:
fill().

* Applying styles and colors:

*color:*
There are two important properties we can use: fillStyle and strokeStyle.
1- fillStyle = color: Sets the style used when filling shapes.
2- strokeStyle = color: Sets the style for shapes' outlines.

*Line styles:*
There are several properties which allow us to style lines:

1- lineWidth = value: Sets the width of lines drawn in the future.
2- lineCap = type: Sets the appearance of the ends of lines.
3- lineJoin = type: Sets the appearance of the "corners" where lines meet.
4- miterLimit = value: Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
5- getLineDash(): Returns the current line dash pattern array containing an even number of non-negative numbers.
6- setLineDash(segments): Sets the current line dash pattern.
7- lineDashOffset = value: Specifies where to start a dash array on a line.

* Drawing text:
There are two methods to render text:

1- fillText(text, x, y [, maxWidth]): Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
2- strokeText(text, x, y [, maxWidth]): Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.