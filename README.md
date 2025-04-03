# calculator-from-html-css-js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        button {
            padding: 20px;
            border: 2px solid black;
            border-radius: 10px;
            font-size: 1.4rem;
            margin: 3px;
            flex-basis: 25%; 
            box-sizing: border-box;
        }
        h1 {
            text-align: center;
        }
        .container {
            max-width: 250px;
            margin: auto;
        }
        .row {
            display: flex;
            justify-content: center;
        }
        .show {
            width: 100%;
            padding: 6px;
            border: 2px solid black;
            border-radius: 5px;
            font-size: 1.2rem;
            margin-bottom: 8px;
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <h1>Calculator</h1>
    <div class="container">
        <div class="row display">
            <input type="text" class="show" readonly>
        </div>
      
        <div class="row">
            <button class="button">7</button>
            <button class="button">8</button>
            <button class="button">9</button>
            <button class="button">*</button>
        </div>
        <div class="row">
            <button class="button">4</button>
            <button class="button">5</button>
            <button class="button">6</button>
            <button class="button">/</button>
        </div>
        <div class="row">
            <button class="button">1</button>
            <button class="button">2</button>
            <button class="button">3</button>
            <button class="button">+</button>
        </div>
        <div class="row">
            <button class="button">0</button>
            <button class="button">.</button>
            <button class="button">=</button>
            <button class="button">-</button>
        </div>
        <div class="row">
            <button class="button">C</button>
            
            
        </div>
    </div>
    <script>
        let a="";
        let buttons=document.querySelectorAll("button");
        for(var i=0;i<buttons.length;i++)
    {
        document.querySelectorAll("button")[i].addEventListener("click",function(){
          
            if(this.innerHTML=="=")
        {
            a=eval(a);
            document.querySelector(".show").value=a;
        }
        else if(this.innerHTML=="C")
        {
            a="";
            document.querySelector(".show").value=a;
        }
        else{
            a=a+this.innerHTML;
            document.querySelector(".show").value=a;
        }
        });

    }
    </script>
</body>
</html>
