<img src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph20.png" />

# Kalman Filter
The graph above shows measurements taken from the internal temperature sensor of a Raspberry Pi, with some random noise added artificially. The black line is the measurement plot (with noise), green is a Kalman implementation with what seems like appropriate values for smoothing, as below:

r1 =  4, q1 = 5   (RED)
r2 = 22, q2= 0.5  (GREEN)
