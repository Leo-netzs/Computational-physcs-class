# Activity 1
This activity is based on the resolution of 4 questions given in the computational physics class of the UFU postgraduate program in 2025

The solved questions are described below

## Exercise 1

Implement the gradient descent algorithm to find the minimum of the function $U(x) = x^2 -1$. This is a very simple case for which we know the exact solution. Illustrate the algorithm with a graph showing the function $U(x)$ and the trajectory of the particle. Initially use a learning rate $\alpha = 0.1$ and a tolerance $\epsilon = 0.01$. The maximum number of iterations should be 1000. The initial position of the particle should be $x_{0} = 5$. Then, vary these parameters to see how they affect the convergence of the algorithm.

## Exercise 2

Repeat exercise 1 for the function $U(x) = x^2 (x-1)(x+1)$. This function has two global minima. Use $x_{0} = 2$ and try to adjust $\alpha$ to try to make the code converge sometimes in one minimum, sometimes in the other. What happens? What can you conclude about the choice of the learning rate $\alpha$?


## Exercise 3

Repeat exercise 2, but now let's manipulate the height of the minima by summing a line in $U(x)$, such that the function is now $U(x) = x^2 (x-1)(x+1) + x/4$. What happens? What can you conclude about the choice of the learning rate $\alpha$?

## Exercise 4

Now consider a two-dimensional function $U(\vec{r}) = U(x,y) = \sin(x)\cos(y) + 2 (xy)^2/1000$. The function has multiple local minima. The 3D visualization of the steps in this case can be difficult to interpret. So, in this case, to follow the evolution of the algorithm, make two graphs:

a. A contour plot (use `plt.imshow` or `plt.pcolormesh`) of the function $U(x,y)$ and draw the trajectory of the particle on the graph.

b. Make a graph of the value of $U(x_{n}, r_{n})$ at each step as a function of the iterations (steps) $n$. In the context of neural networks we will call these steps **epochs**.

Vary the starting position $(x_{0}, y_{0})$ and the learning rate $\alpha$ and see how this affects the convergence of the algorithm. What happens if you increase the learning rate a lot? What if you decrease it a lot? Can you reach the global minimum?


## Answers:

* 2:
    
    The gradient function can fall into any of the wells depending on the value of the learning rate, for higher values ​​the gradient function explodes, and there is no possible solution to the problem, for low values ​​the function falls into the closest well, for intermediate values ​​the function falls into the furthest well, and for a given value x the function oscillates from one side to the other without falling into any of the minima, or exploding.

* 3:

    In this case the function went to the global minimum, not getting stuck at the closest local minimum, with the increase in the learning rate the function jumps further away which hinders the finding of the local minimum, and with much smaller values ​​the function may not reach the global minimum, which can be corrected by increasing the number of maximum iterations

* 4:

    O ChatGPT disse:
A too high learning rate causes the algorithm to overshoot or diverge, while a very low one makes convergence slow. An optimal value ensures stable descent. Since U(x,y) has many local minima, gradient descent may not find the global minimum unless multiple random starting points are used.
