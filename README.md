# WALESKA-1-REPERTORIO
CALCULADORA SIMPLES
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; }
        .calculator { width: 300px; margin: 100px auto; padding: 20px; background: #fff; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        input[type="text"] { width: 100%; height: 40px; text-align: right; border: 1px solid #ddd; border-radius: 5px; padding: 10px; font-size: 18px; }
        button { width: 20%; height: 40px; margin: 5px; border: none; background: #007BFF; color: white; font-size: 18px; border-radius: 5px; cursor: pointer; }
        button:hover { background: #0056b3; }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" disabled />
        <div>
            <button onclick="clearResult()">C</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('/')">/</button>
        </div>
        <div>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('*')">*</button>
        </div>
        <div>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="calculate()">=</button>
        </div>
        <div>
            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('-')">-</button>
        </div>
    </div>
    <script>
        function appendValue(value) {
            document.getElementById('result').value += value;
        }
        function clearResult() {
            document.getElementById('result').value = '';
        }
        function calculate() {
            const resultField = document.getElementById('result');
            try {
                resultField.value = eval(resultField.value);
            } catch (e) {
                resultField.value = 'Error';
            }
        }
    </script>
</body>
</html>
