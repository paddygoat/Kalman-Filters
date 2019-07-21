# Kalman Filter

<p></p>
<p>This is the main bit of code that was used to build the filter, derived from <a href="https://www.kalmanfilter.net/default.aspx" target="_blank">Alex's tutorial</a>:</p>

<figure><img class="lazy" src="https://cdn.hackaday.io/images/5029601563614846858.jpg">The Jupityer notebook can be downloaded from Github <a href="https://github.com/paddygoat/Kalman-Filters/blob/master/Kalman_Temperatures_Pi_Internal_Sensor.ipynb" target="_blank">HERE</a>.<br>There are 2 constants to 'play about with', namely 'r' and 'q' and here are some of my results with different values. The r value is measured off the black curve and is the variance<sup>2</sup> and in this case = 5<sup>2</sup> = 25. The values of q are just guessed, to stimulate the filter into becoming dynamic. The original readings, with a bit of noise added, are always in black.<br></figure>

<figure><img class="lazy" src="https://github.com/paddygoat/Kalman-Filters/blob/master/graph24.jpg"><p>The graph above shows results during which the Pi was put under load (training a neural network) and then unloaded again.
<br>TempPi = BLACK, <br></p>
<p>Kalman_1 = RED, r1 = 25, q1 = 0.01,<br></p>
<p>Kalman_2 = GREEN, r2 = 25, q2= 0.1,<br></p>
<p>Kalman_3 = BLUE, r3 = 25, q3= 0.5,<br></p>
<p>Kalman_4 = ORANGE, r4 = 25, q4= 5.<br></p>
<p>The green curve is obviously not very useful, and the red curve shows quite good smoothing but seems to lag behind the black curve somewhat when the temperature is changing quickly. The blue and orange curves seem to reduce the noise quite effectively with no discernible lag but are not particularly smooth. The orange curve shows noise reduction of about 50% and the blue of about 90%</p>
<p>The filter certainly seems to be capable of reducing noise, but as soon as it is used 'aggressively' it demonstrates lag.<br><br></p></figure>
