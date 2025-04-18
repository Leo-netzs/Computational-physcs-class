# Activity 2

## class particle

In this activity, we will explore the fundamentals of object-oriented programming in Python. We will create a class called Particle that represents a particle in a two-dimensional space. The class should have the following attributes and methods:7

* atributes

    `x` particle x coordenates

    `y` particle y coordenates

    `vx`particle x velocity

    `vy`particle y velocity

    `mass` particle mass

* methods 

    `__init__(self, x, y,  vx, vy, mass)`, contructor of class who initialize the particle atributes

    `newton(self, fx, fy, dt)`: Apply the Newton second law to atualize the velocity and the position of the particle based on the forces `(fx, fy)` apllied in the time interval `dt`. consider that the forces are constant in the time interval `dt`

## exemple 1: oblique throw

Create the particle initially with position (x,y) = (0,0), velocity (vx,vy) = (10,10) m/s, and mass m = 1 kg. We will consider only the force of gravity, (fx, fy) = (0, -9.8) m/s². Every dt = 0.1 s, apply the force of gravity and update the position and velocity of the particle. Save the position, velocity and time in lists or arrays for later plotting. Stop the loop when the particle hits the ground (y <= 0). Plot the position as a function of time.