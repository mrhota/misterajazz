---
title: "Coin Flip Advisor"
description: "A (crappy) tool to help you apologize."
date: 2023-09-23T16:10:10-04:00
---

# Coin Flip Advisor

Need to flip a coin? Well, you've got a lot of things to consider. What's the landing surface like? What's the temperature where you'll be flipping your coin? Are any fans turned on? What's the relative humidity? What about the coin itself? How much does it weigh? Does it have smooth edges? What are its dimensions? On and on!

It's enough to make you want to throw your hands up instead of the coin!

But what if you could take the guess work out of coin flips?

Well, look no further! We can help you flip with confidence. Just enter the relevant information below and we'll tell you whether to you'll end up with heads or tails.

{{< loadJS "c" >}}

<form id="coin-flip-form">
  <label for="surface-texture">Landing Surface Texture:</label>
  <select id="surface-texture" name="surface-texture">
    <option value="hardwood">Hardwood</option>
    <option value="carpet">Carpet</option>
    <option value="tile">Tile</option>
    <option value="brick">Brick</option>
  </select>

<label for="temperature">Temperature (°F):</label>
<input type="number" id="temperature" name="temperature" min="-50" max="150" step="0.1">

<label for="fan-status">Is a fan turned on?</label>
<input type="checkbox" id="fan-status" name="fan-status">

<label for="humidity">Relative Humidity (%):</label>
<input type="number" id="humidity" name="humidity" min="0" max="100" step="0.1">

<label for="coin-diameter">Coin Diameter (mm):</label>
<input type="number" id="coin-diameter" name="coin-diameter" min="0" step="0.01">

<label for="coin-thickness">Coin Thickness (mm):</label>
<input type="number" id="coin-thickness" name="coin-thickness" min="0" step="0.01">

<label for="coin-weight">Coin Weight (g):</label>
<input type="number" id="coin-weight" name="coin-weight" min="0" step="0.01">

<label for="edge-type">Coin Edge Type:</label>
<select id="edge-type" name="edge-type">

  <option value="smooth">Smooth</option>
  <option value="reeded">Reeded</option>
  <option value="lettered">Lettered</option>
</select>

<label for="wind-heading">Wind Heading (degrees):</label>
<input type="number" id="wind-heading" name="wind-heading" min="0" max="360" step="0.1">

<label for="wind-speed">Wind Speed (mph):</label>
<input type="number" id="wind-speed" name="wind-speed" min="0" step="0.1">

<label for="flip-height">Desired Flip Height (m):</label>
<input type="number" id="flip-height" name="flip-height" min="0" step="0.01">

<label for="number-of-turns">Desired Number of Turns in Air:</label>
<input type="number" id="number-of-turns" name="number-of-turns" min="0" step="0.1">

<input id="submit-button" type="submit" value="Predict Flip Outcome">
</form>

<div id="result" style="display:none;"></div>

<script type="text/javascript">
  mrhota.alphabetsuperset.c.main();
</script>
