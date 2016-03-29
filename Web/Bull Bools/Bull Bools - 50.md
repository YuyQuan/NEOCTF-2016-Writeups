<b> Problem: </b> <br>
How bout that picture of that bull??

[162.243.0.171/Bull.php](162.243.0.171/Bull.php)

<b>tl;dr</b><br>
Open the console.

<b> Solution: </b> <br>

Once again, we are given a webpage with a single button on it. Checking the source reveals a form is sending the value false to Bull.php

Since the name of the problem is Bull Bools, we can assume that we have to change this value to true. Fortunately, this is extremely easy in any web browser. For example in Chrome, we can right click on the button and click inspect. We simply click on false in the developer console and change it to true. Once we do so, we are presented wit the flag

Flag: flag{G0t_D@T_F1@g}


<b> Writeup by Nick DeFilippis </b>


