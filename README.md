# bmi-calculator

EXP 08 - CREATE A BMI CALCULATOR


AIM:
To create a BMI calculator using react js.

SOFTWARE:
Visual Studio Code

ALGORITHM
Create a new project using Create React App or your preferred method. Set up the necessary dependencies.
In your components directory, create a new file called "BMICalculator.js". Import the necessary React dependencies.
Define the BMICalculator component
Open your App.js file.Import the BMICalculator component
Use the BMICalculator component in the main App component
Run your React.js development server to see the BMI calculator in action.
PROGRAM:
java

import React, { useState } from 'react';

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBMI] = useState(null);

  const calculateBMI = () => {
    const heightInMeters = height / 100;    
    const bmiValue = weight / (heightInMeters * heightInMeters);
    setBMI(bmiValue.toFixed(2));
  };

  return (
    <div>
      <h2>BMI Calculator</h2>
      <div>
        <label htmlFor="weight">Weight (kg):</label>
        <input
          type="text"
          id="weight"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
        />
      </div>
      <div>
        <label htmlFor="height">Height (cm):</label>
        <input
          type="text"
          id="height"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
        />
      </div>
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <p>Your BMI is: {bmi}</p>}
    </div>
  );
}

export default BMICalculator;
OUTPUT:

![image](https://github.com/Shinysudhakar/bmi-calculator/assets/127575325/590b045e-532b-4e49-8231-aa3d1991caf6)

After the calculation

![image](https://github.com/Shinysudhakar/bmi-calculator/assets/127575325/9e45ac12-b836-408c-ba78-43a14c44f1e0)


RESULT:
Thus the BMI calculator is created.
