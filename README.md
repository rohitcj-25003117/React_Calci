# Ex04 Simple Calculator - React Project
## Date: 17-03-2026

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
-
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
### Calculatr.jsx

```
import React, { useState } from "react";
import "./Calculator.css";
-
function Calculator() {

  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input className="display" type="text" value={input} readOnly />

      <div className="buttons">

        <button onClick={clearInput}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={calculate}>=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")}>0</button>

      </div>
    </div>
  );
}

export default Calculator;
```

### Calculator.css
```
.calculator {
  width: 300px;
  margin: 50px auto;
  padding: 20px;
  background: #1e1e1e;
  border-radius: 10px;
  text-align: center;
}

.display {
  width: 100%;
  height: 50px;
  margin-bottom: 10px;
  font-size: 20px;
  text-align: right;
  padding-right: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  cursor: pointer;
  border: none;
  background: #444;
  color: white;
  border-radius: 5px;
}

button:hover {
  background: #666;
}
```

### App.js
```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <h1 style={{textAlign:"center"}}>Simple React Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;
```
## OUTPUT
<img width="1885" height="962" alt="image" src="https://github.com/user-attachments/assets/d85ac343-952a-4f4e-8fde-6fa2dce9c214" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
