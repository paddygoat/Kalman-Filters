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


<p></p>
<p>This is the main bit of code that was used to build the filter, derived from <a href="https://www.kalmanfilter.net/default.aspx" target="_blank">Alex's tutorial</a>:</p>

<figure><img class="lazy" src="https://cdn.hackaday.io/images/5029601563614846858.jpg">The Jupityer notebook can be downloaded from Github <a href="https://github.com/paddygoat/Kalman-Filters/blob/master/Kalman_Temperatures_Pi_Internal_Sensor.ipynb" target="_blank">HERE</a>.<br>There are 2 constants to 'play about with', namely 'r' and 'q' and here are some of my results with different values. The original readings, with a bit of noise added, are always in black.<br></figure>

<figure><img class="lazy" src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph24.jpg"><p>The graph above shows results during which the Pi was put under load (training a neural network) and then unloaded again.
<br>TempPi = BLACK, <br></p>
<p>Kalman_1 = RED, r1 = 50, q1 = 0.1,<br></p>
<p>Kalman_2 = GREEN, r2 = 100, q2= 0.01,<br></p>
<p>Kalman_3 = BLUE, r3 = 25, q3= 0.5,<br></p>
<p>Kalman_4 = ORANGE, r4 = 10, q4= 1.<br></p>
<p>The green curve is obviously not very useful, and the red curve shows quite good smoothing but seems to lag behind the black curve somewhat when the temperature is changing quickly. The blue and orange curves seem to reduce the noise quite effectively with no discernible lag but are not particularly smooth. The orange curve shows noise reduction of about 50% and the blue of about 90%</p>
<p>The filter certainly seems to be capable of reducing noise, but as soon as it is used 'aggressively' it demonstrates lag.<br><br></p></figure>
