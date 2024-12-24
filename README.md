# Probability-Calculator
This Python program simulates a random ball drawing experiment using a Hat class and an experiment function. The program allows you to define a hat filled with balls of various colors, and then perform multiple experiments where a specified number of balls are drawn randomly. The program calculates the probability of drawing a specified number of each color based on the results of multiple trials.

## Features
### Hat Class
The Hat class represents a collection of balls in a hat. The class includes methods to initialize the contents of the hat and draw balls randomly.

### Attributes:

- contents: A list holding the balls in the hat. The balls are represented by their color, and each color may appear multiple times based on the count specified during initialization.

### Methods:

- __init__(self, **kwargs): Initializes the hat's contents based on keyword arguments where the key is the ball color and the value is the count of balls of that color.
- draw(self, num_of_balls): Draws a specified number of balls from the hat:
  - If the number of balls requested exceeds the total number of balls in the hat, all balls are drawn and the hat is emptied.
  - If the number of balls requested is less than the total, a random sample is drawn and removed from the hat.

### Experiment Function
The experiment function simulates multiple trials of drawing balls from a hat, checking how often the drawn balls meet a specified expectation, and calculates the probability of success.

### Parameters:

- hat: The Hat object that contains the balls.
- expected_balls: A dictionary specifying the colors and counts of balls expected to be drawn (e.g., {'red': 2, 'blue': 1}).
- num_balls_drawn: The number of balls to draw in each experiment.
- num_experiments: The number of experiments to conduct.

### Return Value:

The function returns the probability of drawing the specified number of each color ball in the trials. It calculates the ratio of successful experiments (where the drawn balls meet the expected criteria) to the total number of experiments.
