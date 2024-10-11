<!DOCTYPE html>
<html lang="vi">

<head>
    <style>
     body {
    font-family: 'Arial', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.calculator {
    width: 400px;
    background-color: #e0e0e0;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
}

.display {
    text-align: right;
    margin-bottom: 20px;
    background-color: #b0c4de;
    padding: 10px;
    border-radius: 5px;
}

.display input {
    width: 93%;
    padding: 15px;
    font-size: 24px;
    background-color: #6e6868;
    border: none;
    color: black;
    border-radius: 5px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 10px;
}

button {
    padding: 20px;
    font-size: 18px;
    border: none;
    background-color: #555;
    color: white;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

button:hover {
    background-color: #777;
}

.equal-button {
    grid-column: span 1;
    background-color: #ff9800;
    color: white;
    grid-row: span 2;
}

.equal-button:hover {
    background-color: #ff9800;
}

.zero-button {
    grid-column: span 2;
}
    </style>
</head>

<body>
    <!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Máy tính điện tử</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <div class="display">
            <input type="text" id="result" disabled>
        </div>
        <div class="buttons">
        
            <button onclick="clearDisplay()">MC</button>
            <button onclick="appendMemory()">M+</button>
            <button onclick="appendNumber('+')">+</button>
            <button onclick="appendNumber('*')">X</button>

            <button onclick="appendNumber('7')">7</button>
            <button onclick="appendNumber('8')">8</button>
            <button onclick="appendNumber('9')">9</button>
            <button onclick="appendNumber('-')">-</button>

        
            <button onclick="appendNumber('4')">4</button>
            <button onclick="appendNumber('5')">5</button>
            <button onclick="appendNumber('6')">6</button>
            <button onclick="appendNumber('+')">+</button>

            
            <button onclick="appendNumber('1')">1</button>
            <button onclick="appendNumber('2')">2</button>
            <button onclick="appendNumber('3')">3</button>
            <button rowspan="2" class="equal-button" onclick="calculate()">=</button>

            
            <button onclick="appendNumber('0')" class="zero-button">0</button>
            <button onclick="appendNumber('.')">.</button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
        </div>

        <script>
         function clearDisplay() {
    document.getElementById('result').value = '';
}z

function appendNumber(number) {
    document.getElementById('result').value += number;
}

function deleteNumber() {
    let currentValue = document.getElementById('result').value;
    document.getElementById('result').value = currentValue.slice(0, -1);
}

function calculate() {
    let result = document.getElementById('result').value;
    try {
        document.getElementById('result').value = eval(result);
    } catch (e) {
        document.getElementById('result').value = 'Error';
    }
}
        </script>
</body>
