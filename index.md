## NOTES ON EDX TINYML

### 1. Explicit Coding
- Defining rules that determine the behaviour of the program.
- Everything is precalculated and predetermined by the programmer.
- Scenarios are limited by complexity.

![image](https://user-images.githubusercontent.com/26565418/99030586-6e8fab80-259b-11eb-972b-197edbcb8857.PNG)

Consider Human Activity Detection, how would we make sure that the man is golfing?
![image](https://user-images.githubusercontent.com/26565418/99030675-a5fe5800-259b-11eb-8cb6-4200ddb6409e.png)

Machine Learning could solve this problem. We can gather lots of sensor data and map them to activity that user is performing.
![image](https://user-images.githubusercontent.com/26565418/99031070-27ee8100-259c-11eb-9edf-dd425fcfddf5.png)

We could use APIs that allow us to find distinguished patterns such as the four bits in every category which makes them apart from one another.

First, the computer will make a guess as to the relationship between the data and its labels.
It does this by randomly initializing a neural network, guesses the relationship between input-labels and measures how good or bad the guess is, which is further optimized for better predictions. We try to minimize the loss with each epoch to obtain high, accurate results. - Learning from Experience

![image](https://user-images.githubusercontent.com/26565418/99031506-4608b100-259d-11eb-95f0-ffc2d722f0a5.png)

We can use square the Euclidean Distance between our guess and the real output(Y) mapped to an input x.

![image](https://user-images.githubusercontent.com/26565418/99032223-05119c00-259f-11eb-815f-54b331690440.png)

Eventually our loss will become zero and our guess = real label. 
[Exploring Loss](https://github.com/Shruti2301/TinyML/blob/gh-pages/ExploringLoss.ipynb)

### 2. Minimizing Loss

1. You make a guess.
2. You measure how accurate that guess is by calculating its loss and then you use that data to make another guess
   with the next guess usually being a little bit better than the current one.
3. The idea is that the smaller the loss, the more accurate your guess is.

Our Loss function is the square of the Euclidean Distance. Square functions have a parabolic shape and its minimum is at the bottom of parabola.

### Gradient -

If we differentiate the values with respect to the loss function, we'll get a gradient which could be used to determine direction
towards the bottom of parabola. 

### Learning Rate -

Once we know what the direction is, we can pick a step size. The step size is often called the learning rate.
So given a direction from the gradient and a step size from the learning rate, we can safely take a step towards the minimum.
We repeat this process and end up in global minima, the minimum bottom point of parabola.

Choosing LR is very important - if it's too large, we could overshoot or is too small, it might take a long time to reach the minimum.

### QUIZ 1 - 
Which of the following are true about learning rates?
![image](https://user-images.githubusercontent.com/26565418/99035576-f8447680-25a5-11eb-901a-3cfe83f00fcf.png)

We can improve our model by?
![image](https://user-images.githubusercontent.com/26565418/99035612-0b574680-25a6-11eb-9189-41bd61d77e1b.png)

Machine Learning Algorithms have
![image](https://user-images.githubusercontent.com/26565418/99035643-1c07bc80-25a6-11eb-8ddd-2895696647ac.png)
