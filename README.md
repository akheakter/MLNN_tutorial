# Network Depth vs Width: The Architecture Decision That Makes or Breaks Your Model

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

A comprehensive tutorial exploring how neural network architecture choices (depth vs width) affect performance across different problem complexities.

##  Tutorial Overview

This tutorial demonstrates that **how you distribute your parameter budget matters more than the total number of parameters**. Through controlled experiments, we show when to choose deep & narrow vs shallow & wide architectures.

### Key Findings
- **Simple problems**: Architecture choice doesn't matter much
- **Moderate complexity**: Deep & narrow networks perform better (99.5% vs 98.5%)
- **Complex problems**: Multiple architectures can succeed, but with different learning patterns

##  Quick Start

### Option 1: View Tutorial Online
1. Open `html_slide_tutorial/network_depth_width_tutorial.html` in your browser
2. Navigate with arrow keys or click buttons
3. Interactive presentation with all results

### Option 2: Run Experiments Yourself
```bash
# Clone repository
git clone https://github.com/akheakter/MLNN_Tutorial
cd Machine-Learning-Tutorial

# Install dependencies
pip install -r requirements.txt

# Run experiments
python code/network_depth_width_tutorial.py
```
## Tutorial Contents
1. The Parameter Budget Challenge
Learn why distributing 5,000 parameters differently can mean 60% vs 95% accuracy.
2. Three Architecture Strategies

Deep & Narrow (Skyscraper): 64→32→16→8 layers
Shallow & Wide (Stadium): 128 neurons in single layer
Balanced (Office): 64→32 layers

3. Experimental Results
Controlled comparison across three complexity levels:

Simple: Linearly separable data
Moderate: Non-linear patterns with noise
Complex: High-dimensional synthetic data

4. Practical Guidelines
Decision framework for choosing architectures in real projects.
## Requirements

Python 3.8+
TensorFlow 2.x
scikit-learn
matplotlib
seaborn
pandas
numpy

## Repository Structure

html_slide_tutorial/ - Interactive HTML tutorial and assets
experiments/ - Complete experimental implementation
data/ - Experimental results and datasets
docs/ - Methodology and references

## Educational Objectives
After completing this tutorial, you will:

Understand the depth vs width trade-off in neural networks
Know when to choose each architecture strategy
Be able to implement controlled architecture experiments
Have practical guidelines for real-world projects

## References

See [references.md]('https://github.com/akheakter/Machine-Learning-Tutorial/blob/master/docs/references.md')

## Contributing
This tutorial was created for educational purposes. If you find errors or have suggestions:

## Open an issue
Submit a pull request
Contact the author

## License
This project is licensed under the MIT License - see the LICENSE file for details.
## Author
Akhe Akter
University Course: Machine Learning and Neural Networks
Date: June 2025
## Acknowledgments

Course instructors and teaching assistants
TensorFlow and scikit-learn communities
Universal approximation theorem researchers


If this tutorial helped you understand neural network architecture design, please star this repository!
