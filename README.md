# Kalman Filter
<img src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph20.png" />

The graph above shows measurements taken from the internal temperature sensor of a Raspberry Pi, with some random noise added artificially. The black line is the measurement plot (with noise), green is a Kalman implementation with what seems like appropriate values for smoothing, as below:

r1 =  4, q1 = 5   (RED)
r2 = 22, q2= 0.5  (GREEN)


<img src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph21.png" />
TempPi = BLACK, 
Kalman_1 = RED, 
Kalman_2 = GREEN, 
Kalman_3 = BLUE, 
Kalman_4 = ORANGE, 
r1 =  50, q1 = 0.1, 
r2 = 100, q2= 0.01, 
r3 = 40, q3= 5, 
r4 = 22, q4= 20.
<img src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph23.png" />
The graph above shows results during which the Pi was put under load (traing a neural network) and then unloaded again.
TempPi = BLACK, 
Kalman_1 = RED, 
Kalman_2 = GREEN, 
Kalman_3 = BLUE, 
Kalman_4 = ORANGE, 
r1 =  50, q1 = 0.1, 
r2 = 100, q2= 0.01, 
r3 = 40, q3= 5, 
r4 = 22, q4= 20.
