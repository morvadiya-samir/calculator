<!DOCTYPE html>
<html lang="en">

<head>
    <title>calculator</title>
    <style>
        * {
            font-family: sans-serif;
            font-size: 1rem;
        }

        label {
            display: inline-block;
            wclassth: 62px;
            margin: 10px;
        }

        button {
            padding: 10px;
            padding-left: 25px;
            padding-right: 25px;
            border: 2px solid black;
            border-radius: 2rem;
            display: inline;
            /* hei */
            width: 100px;
            margin: 10px;
            background-color: slategray;
            color: white;

        }

        button:hover {
            box-shadow: 1px 1px 15px 5px white;
        }

        .container {
            text-align: center;
            margin: auto;
            padding-top: 9%;
        }

        .cal {
            border-radius: 1rem;
            margin: auto;
            display: inline-block;
            border: 2px solid black;
            padding: 15px;
            background-color: black;
        }

        #display {
            border: 2px solid black;
            border-radius: 1rem;
            margin-bottom: .5rem;
        }

        input[type=text] {
            width: 21.5rem;
            height: 3rem;
            font-size: 2rem;
            margin-left:1rem ;

        }

        input::-webkit-outer-spin-button,
        input::-webkit-inner-spin-button {
            -webkit-appearance: none;
        }
    </style>
</head>

<body>
    <div class="container">

        <div class="cal">

            <input type="text" id="display">
            <button type=" button" class="btn" onclick="clearScreen()" value="">CE</button><br>
            <button type=" button" class="btn" onclick="display('1')" value="">1</button>
            <button type=" button" class="btn" onclick="display('2')" value="">2</button>
            <button type=" button" class="btn" onclick="display('3')" value="">3</button>
            <button type=" button" class="btn" onclick="display('*')" value="">*</button><br>
            <button type=" button" class="btn" onclick="display('4')" value="">4</button>
            <button type=" button" class="btn" onclick="display('5')" value="">5</button>
            <button type=" button" class="btn" onclick="display('6')" value="">6</button>
            <button type=" button" class="btn" onclick="display('-')" value="">-</button><br>
            <button type=" button" class="btn" onclick="display('7')" value="">7</button>
            <button type=" button" class="btn" onclick="display('8')" value="">8</button>
            <button type=" button" class="btn" onclick="display('9')" value="">9</button>
            <button type=" button" class="btn" onclick="display('+')" value="">+</button><br>
            <button type=" button" class="btn" onclick="display('/')" value="">/</button>
            <button type=" button" class="btn" onclick="display('0')" value="">0</button>
            <button type=" button" class="btn" onclick="display('.')" value="">.</button>
            <button type=" button" class="btn" onclick="calculate()" value="">=</button>

        </div>
    </div>
    <script>

        function clearScreen() {
            document.getElementById("display").value = "";
        }
        
        function calculate() {
            var p = document.getElementById("display").value;
            var q = eval(p);
            document.getElementById("display").value = q;
        }
        function display(num) {
            document.getElementById("display").value += num;
        
        }
    </script>
</body>

</html>
