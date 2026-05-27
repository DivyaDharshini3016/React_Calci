# Ex04 Simple Calculator - React Project
## Date: 27/05/2026

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
### App.jsx
```
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <Calculator />
    </div>
  );
}

export default App;
```
### Calculator.jsx
```
import { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h2>Simple Calculator</h2>

      <input
        type="text"
        value={input}
        readOnly
        className="display"
      />

      <div className="buttons">
        <button onClick={clearInput}>C</button>
        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("/")}>/</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("*")}>*</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={() => handleClick(".")}>.</button>
        <button onClick={calculateResult}>=</button>
        <button onClick={() => handleClick("+")}>+</button>
      </div>
    </div>
  );
}

export default Calculator;
```
### Calculator.css
```
body {
  background-color: #f2f2f2;
  font-family: Arial, sans-serif;
}

.calculator {
  width: 300px;
  margin: 50px auto;
  padding: 20px;
  background: rgb(18, 12, 12);
  border-radius: 10px;
  text-align: center;
  box-shadow: 0px 0px 10px rgb(8, 6, 6);
}

.display {
  width: 100%;
  height: 50px;
  margin-bottom: 20px;
  font-size: 22px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  border: none;
  background-color: green;
  color: white;
  border-radius: 5px;
  cursor: pointer;
}

.calculator h2 {
  color: rgb(71, 7, 198);
}

```

## OUTPUT

<img width="1082" height="820" alt="image" src="https://github.com/user-attachments/assets/c8288606-0765-4d5d-bde8-4b1946331506" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
