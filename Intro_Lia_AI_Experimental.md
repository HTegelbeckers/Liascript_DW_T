<!--

author:   Hannes Tegelbeckers
email:    hannes.tegelbeckers@ovgu.de
version:  0.0.1
language: de
narrator: Deutsch Female

link:     https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css

import: https://raw.githubusercontent.com/LiaTemplates/Rextester/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/WebDev/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/NetSwarm-Simulator/master/README.md
import: https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md

#### Preview Lia
<html>
  <head>
    <script type="text/javascript" src="https://liascript.github.io/course/preview-lia.js"></script>
  </head>
  <body>
    ...
    <preview-lia src="https://raw.githubusercontent.com/liaScript/docs/master/README.md">
    </preview-lia>

    <preview-lia src="https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md">
    </preview-lia>

    ...
  </body>
</html>

https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md#5
https://LiaScript.github.io/course/?YOUR_RAW_COURSE_URL.md
-->
# Introduction to AI
Artificial Intelligence (AI) is the simulation of human intelligence by computers. It includes learning, reasoning, and self-correction.


# What is Machine Learning?
A subset of AI, Machine Learning allows computers to learn from data rather than being explicitly programmed.

# Types of Machine Learning
1. Supervised Learning
2. Unsupervised Learning
3. Reinforcement Learning

# Decision Trees

A simple yet powerful Machine Learning algorithm. It splits the data into subsets to make decisions.

## JavaScript Example: Simple Decision Tree

```javascript
// Sample data: [height, weight]
const data = [
  { features: [5.0, 150], label: "short" },
  { features: [5.2, 152], label: "short" },
  { features: [6.0, 180], label: "tall" },
  { features: [5.5, 145], label: "short" },
  { features: [5.9, 175], label: "tall" }
];

// Simple Decision Tree Classifier (Hypothetical)
function classify(features) {
  if (features[0] > 5.5) {
    return "tall";
  } else {
    return "short";
  }
}

const prediction = classify([5.8, 160]);
console.log("Predicted label:", prediction);

### Slide 5: Overfitting and Underfitting (Enhanced)

// Sample data
const x = [1, 2, 3, 4, 5];
const y = [2, 4, 1, 3, 5];

// Linear Regression Model (Hypothetical)
function predict(x) {
  return 1.2 * x + 0.5;
}

// Plotting (Hypothetical)
// Code to plot the data points and the prediction line

#Bias-Variance Tredeoffe
// Code to demonstrate the Bias-Variance tradeoff
// (This would ideally show how changing model complexity affects bias and variance)

# Bias and Variance

- High Bias: Underfitting
- High Variance: Overfitting

## JavaScript Example: Bias-Variance Tradeoff

```javascript
// Sample data
const x = [1, 2, 3, 4, 5];
const y = [2.1, 3.9, 3.1, 4.0, 5.2];  // Slightly noisy data

// Polynomial Regression of Degree 1 (Linear)
function predict1(x) {
  return 1 * x + 1;
}

// Polynomial Regression of Degree 2
function predict2(x) {
  return 1 * x * x + 0.5 * x + 1;
}

// Polynomial Regression of Degree 4 (Overfitting)
function predict4(x) {
  return 0.1 * x * x * x * x - 0.5 * x * x * x + 1 * x * x + 0.5 * x + 1;
}

// Evaluating predictions
const prediction1 = x.map(predict1);
const prediction2 = x.map(predict2);
const prediction4 = x.map(predict4);

// Output or plot these predictions to show how they fit the data


