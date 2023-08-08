# Temp-converter
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=<>, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            padding: 50px 100px;
            background-color: black;
            
        }
        h1{
            text-align: center;
        }
        #container{
            text-align: center;
            background-color: #1abc9c;
            padding: 50px;

        }
        .input-div{
            display: inline-block;
        }
        .inp{
            padding: 5px;
            margin: 10px;
            font-size: 30px;
            font-weight: bold;
            width: 250px;
            text-align: center;
        }
        label{
            font-size: 22px
        }
        h1{
            color: white;
        }
    </style>
</head>

<body>
    <h1>TEMPERATURE CONVERTER</h1>
    <div id="container">
        <div class="input-div"><label>CELSIUS :</label><br><input type="number" value="0" id="cel" class="inp"></div>
        <div class="input-div"><label>FAHRENHEIT :</label><br><input type="number" value="32" id="fah" class="inp"></div>
    </div>

    <script>
        var cel= document.getElementById("cel");
        var fah= document.getElementById("fah");
        cel.addEventListener('input', function(){ 
            console.log("cel changed");
            let c=this.value;
            let f=(c*9/5)+32;
            if(!Number.isInteger(f)){
                f=f.toFixed(4)
            }
            fah.value=f;
        });
        fah.addEventListener('input', function(){
            console.log("fah changed");
            let f=this.value;
            let c=(f-32)*5/9;
            if(!Number.isInteger(c)){
                c=c.toFixed(4)
            }
            cel.value=c;
        });
    </script>
</body>

</html>
