# Bulb Animation

This code creates a simple animation of a light bulb turning on and off. 
The animation is created using two images, one of a light bulb that is off and one of a light bulb that is on. 
When the user clicks the "ON" button, the image of the light bulb that is on is displayed and the background 
color of the page changes to yellow. 
When the user clicks the "OFF" button, the image of the light bulb that is off is 
displayed and the background color of the page changes to black.

## Step-by-Step Explanation

### HTML

The HTML code for this project is relatively simple. 
It consists of a `<div>` element that contains the light bulb image, 
two buttons, and a heading. The `<div>` element is centered both horizontally and 
vertically using the `justify-content` and `align-items` properties. The buttons 
are positioned below the light bulb image using the `margin` property. The heading
is positioned above the light bulb image using the `margin-top` property.

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bulb Animation</title>
    <style>
        body{
            background-color: black;
        }
        .box{
           display: flex;
           justify-content: center;
           height: 100vh;
           align-items: center;
           flex-direction: column;
        }
        button{
            padding: 20px;
            margin: 10px;
            font-family: Georgia, 'Times New Roman', Times, serif;
            border-radius: 7px;
            font-weight: bolder;
            cursor: pointer;
            font-size: 15px;
            color: white;
        }
        #on{
            background-color: green;
        }
        #of{
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="box">
        <h1 id="text"></h1>
        <img src="img/bulb1.png" width="200px" height="300px" id="bulb">
        <button onclick="clickMe('on')" id="on">ON</button>
        <button onclick="clickMe('off')" id="of">OFF</button>
    </div>

    <script>
        function clickMe(state) {
            if (state == 'on'){
                document.getElementById('bulb').setAttribute('src', 'img/bulb2.png');
                document.body.style.backgroundColor= 'yellow';
                document.getElementById('text').innerHTML= 'Light aa gai'
            }else{
                document.getElementById('bulb').setAttribute('src', 'img/bulb1.png');
                document.body.style.backgroundColor= 'black';
            }
        }
    </script>


</body>
</html>
