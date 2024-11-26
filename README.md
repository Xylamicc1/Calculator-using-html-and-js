<html>
<head>
    <script>
        function addition() {
            var x = +document.getElementById('num1').value;
            var y = +document.getElementById('num2').value;
            document.getElementById('result').value = x + y;  
            alert("Addition of two numbers is: " + (x + y));
        }

        function subtraction() {
            var x = +document.getElementById('num1').value;
            var y = +document.getElementById('num2').value;
            document.getElementById('result').value = x - y;  
            alert("Subtraction of two numbers is: " + (x - y));
        }

        function multiplication() {
            var x = +document.getElementById('num1').value;
            var y = +document.getElementById('num2').value;
            document.getElementById('result').value = x * y;  
            alert("Multiplication of two numbers is: " + (x * y));
        }

        function division() {
            var x = +document.getElementById('num1').value;
            var y = +document.getElementById('num2').value;
            if (y === 0) {
                alert("Division by zero is not allowed.");
                document.getElementById('result').value = "Error";
            } else {
                document.getElementById('result').value = x / y;  
                alert("Division of two numbers is: " + (x / y));
            }
        }

        function square() {
            var x = +document.getElementById('num1').value;
            document.getElementById('result').value = x * x;
            alert("Square of the number is: " + (x * x));
        }

        function cube() {
            var x = +document.getElementById('num1').value;
            document.getElementById('result').value = x * x * x;
            alert("Cube of the number is: " + (x * x * x));
        }

        function squareRoot() {
            var x = +document.getElementById('num1').value;
            if (x < 0) {
                alert("Square root of a negative number is not real.");
                document.getElementById('result').value = "Error";
            } else {
                document.getElementById('result').value = Math.sqrt(x);
                alert("Square root of the number is: " + Math.sqrt(x));
            }
        }

        function reset() {
            document.getElementById('formId').reset();
        }
    </script>
</head>
<body>
    <form id="formId">
        <label>Enter First Number:</label>
        <input type="number" id="num1" value="0" required autofocus>
        <br>
        <label>Enter Second Number (optional for addition, subtraction, multiplication, division):</label>
        <input type="number" id="num2" value="0">
        <br>
        <label>Result:</label>
        <input type="text" id="result" value="0" readonly>
        <br>
        <input type="button" onclick="addition()" value="Add">
        <input type="button" onclick="subtraction()" value="Subtract">
        <input type="button" onclick="multiplication()" value="Multiply">
        <input type="button" onclick="division()" value="Divide">
        <input type="button" onclick="square()" value="Square">
        <input type="button" onclick="cube()" value="Cube">
        <input type="button" onclick="squareRoot()" value="Square Root">
        <input type="button" onclick="reset()" value="Reset">
    </form>
</body>
</html>