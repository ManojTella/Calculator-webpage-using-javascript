# Calculator-webpage-using-javascript
### Aim:
To create a calculator webpge using Javascript.
### Program:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <div class="display" id="display"></div>
        <div class="buttons">
            <button onclick="clearDisplay()">AC</button>
            <button onclick="deleteLast()">DEL</button>
            <button onclick="appendCharacter('/')">/</button>
            <button onclick="appendCharacter('*')">*</button>
            <button onclick="appendCharacter('7')">7</button>
            <button onclick="appendCharacter('8')">8</button>
            <button onclick="appendCharacter('9')">9</button>
            <button onclick="appendCharacter('-')">-</button>
            <button onclick="appendCharacter('4')">4</button>
            <button onclick="appendCharacter('5')">5</button>
            <button onclick="appendCharacter('6')">6</button>
            <button onclick="appendCharacter('+')">+</button>
            <button onclick="appendCharacter('1')">1</button>
            <button onclick="appendCharacter('2')">2</button>
            <button onclick="appendCharacter('3')">3</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendCharacter('0')">0</button>
            <button onclick="appendCharacter('.')">.</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
### Styles.css
```
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: linear-gradient(to right, #141E30, #243B55);
    color: #fff;
    font-family: 'Arial', sans-serif;
}

.calculator {
    background: #f0f0f0;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.1);
    width: 300px;
}

.display {
    background: #333;
    color: #fff;
    padding: 30px;
    font-size: 2em;
    border-radius: 10px;
    text-align: right;
    margin-bottom: 10px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

button {
    padding: 20px;
    font-size: 1.5em;
    background: #666;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background: #888;
}
```
### Script.css
```
let display = document.getElementById('display');

function appendCharacter(char) {
    display.innerText += char;
}

function clearDisplay() {
    display.innerText = '';
}

function deleteLast() {
    display.innerText = display.innerText.slice(0, -1);
}

function calculateResult() {
    try {
        display.innerText = eval(display.innerText);
    } catch {
        display.innerText = 'Error';
    }
}
```
### Output:
![Screenshot 2024-07-05 144632](https://github.com/ManojTella/Calculator-webpage-using-javascript/assets/94883876/597cbf66-f62d-44d2-9c2e-89aa72f36a1f)
![Screenshot 2024-07-05 144610](https://github.com/ManojTella/Calculator-webpage-using-javascript/assets/94883876/1faebe8f-4438-41ed-a604-a907a3594c77)
![Screenshot 2024-07-05 144620](https://github.com/ManojTella/Calculator-webpage-using-javascript/assets/94883876/aa0c71ab-4af7-4830-80bd-542eff11ba44)
### Result:
Thus,impletation of calculator webpage using javascript was executed successfully.
