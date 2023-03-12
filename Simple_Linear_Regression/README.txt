1. Consider a simplified fitting problem in the frequency domain where we are looking to find the best fit
of data with a set of periodic (trigonometric) basis functions of the form 1; x; sin(x); cos(x); sin(k *
x); cos(k * x); sin(2 * k * x); cos(2 * k * x); :::, where k is effectively the frequency increment. The
resulting function for a given ”frequency increment”, k, and ”function depth”, d, and parameter vector theta
is then:

y = theta0 * 1 + theta1 * x + Summation(i=1 to i=d)[(theta2*i * sin(i * k * x) + theta2*i+1 * cos(i * k * x))]

For example, if k = 1 and d = 2, your basis (feature) functions are 1; x; sin(x); cos(x); sin(2x); cos(2x),
and we are looking for the best matching parameters theta for the function theta0 + theta1 * x + theta2 * sin(x) +
theta3 * cos(x) + theta4 * sin(2x) + theta5 * cos(2x). This means that this problem can be solved using linear
regression as the function is linear in terms of the parameters theta.
You obtain your value for the ”frequency increment” k and thus your basis functions as part of the data
generation process described above.

a) Implement a linear regression learner to solve this best fit problem for 1 dimensional data. Make
sure your implementation can handle fits for different ”function depths” (at least to ”depth” 6).

b) Apply your regression learner to the data set that was generated for Question 1b) and plot the
resulting function for ”function depth” 0, 1, 2, 3, 4, 5, and 6. Plot the resulting function together
with the data points (using your favorite plotting program, e.g. Matlab, Octave, ...)

c) Evaluate your regression functions by computing the error on the test data points that were generated
for Question 1c). Compare the error results and try to determine for what polynomials overfitting
might be a problem. Which order polynomial would you consider the best prediction function and
why.

d) Repeat the experiment and evaluation of part b) and c) using only the first 20 elements of the training
data set part b) and the Test set of part c). What differences do you see and why might they occur ?