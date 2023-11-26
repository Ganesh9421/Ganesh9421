<!DOCTYPE html>
<html>
<head>
  <title>Simple Calculator</title>
  <style>
    /* Optional: Add some basic styles for better appearance */
    body {
      font-family: Arial, sans-serif;
      text-align: center;
    }
    input[type="text"], input[type="button"] {
      padding: 10px;
      margin: 5px;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <h2>Simple Calculator</h2>
  <input type="text" id="result" disabled><br>
  <input type="button" value="1" onclick="appendToResult('1')">
  <input type="button" value="2" onclick="appendToResult('2')">
  <input type="button" value="3" onclick="appendToResult('3')">
  <input type="button" value="+" onclick="appendToResult('+')"><br>
  <input type="button" value="4" onclick="appendToResult('4')">
  <input type="button" value="5" onclick="appendToResult('5')">
  <input type="button" value="6" onclick="appendToResult('6')">
  <input type="button" value="-" onclick="appendToResult('-')"><br>
  <input type="button" value="7" onclick="appendToResult('7')">
  <input type="button" value="8" onclick="appendToResult('8')">
  <input type="button" value="9" onclick="appendToResult('9')">
  <input type="button" value="*" onclick="appendToResult('*')"><br>
  <input type="button" value="0" onclick="appendToResult('0')">
  <input type="button" value="C" onclick="clearResult()">
  <input type="button" value="=" onclick="calculateResult()">
  <input type="button" value="/" onclick="appendToResult('/')"><br>

  <script>
    function appendToResult(value) {
      document.getElementById("result").value += value;
    }

    function clearResult() {
      document.getElementById("result").value = "";
    }

    function calculateResult() {
      try {
        const expression = document.getElementById("result").value;
        const result = eval(expression);
        document.getElementById("result").value = result;
      } catch (error) {
        document.getElementById("result").value = "Error";
      }
    }
  </script>
</body>
</html>
