layout: page
title: "Tutorial"
permalink: /Tutorial

<!DOCTYPE html>
<html>
<head>
<title>Arduino Temperature Controller</title>
</head>
<body>

<h1>Arduino Temperature Controller</h1>
<p>Say you are a preocess engineer at a brewery, and you need to design a reactor to brew beer at precisly 65&deg;C. However, as part of the brewing process ingrediants are added to the fermenting vessel which drop the temperature. To regain the 65&deg;C brewing temperature you are in need of a temperature controller. 

In this short guide, you will build your own small-scale temperature controlled process, and learn how to tude the controller for stable output. </p>

<h1>What you will need:</h1>
 <ul>
  <li>Breadboard</li>
  <li>Temperature sensor (TMP36 or similar)</li>
  <li>Tupperware container</li>
  <li>Arduino</li>
  <li>12V resistive heating pad</li>
  <li>12V power supply</li>
  <li>Power MOSFET (Logic level N-type)</li>
  
</ul> 

<h1>PID Background</h1>
<p>PID control (Proportional, Integral, Derivative control), is an algorithm that takes some process variable such as temperature, and generates a desired output such as heater voltage. Under feedback control, the output of the controller (heater voltage), affects the input to the controller (temperature). The algorithm used by the controller is called the control law and has the following form:

$$\mathrm{K}_{p}e(t) + \mathrm{K}_{i}\int_{0}^{t}e(\tau)d\tau + \mathrm{K}_{d}\frac{d }{dt}(e(t))$$

Where e(t) is the error function, which is defined as the set point minus the process variable. $$\mathrm{K}_{p}, \mathrm{K}_{i}, \mathrm{K}_{d}$$ are coefficients that determine the relative strength of each term, and are known as proportional gain, integral gain and derivative gain respectivly. In our case, K_d will be set to zero (aka PI control).
</p>

<h1>Set up the temperature sensor:</h1>

Your TMP36 will have three pins: power, data and ground. The power pin may use either +5v or +3.3v. 

The sensor will supply a small voltage to the data pin which is linearly dependant to the temperature of the sensor. 
</body>
</html>
