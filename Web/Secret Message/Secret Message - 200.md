<b> Problem: </b> <br>
You've received a message from Adam! Can you figure out what to do to help him out???<br>
[http://162.243.0.171/Message.html](http://162.243.0.171/Message.html)

<b>tl;dr</b><br>
Go to msg.php and caesar cipher to hex

<b> Solution: </b> <br>

For this problem we are given a website where a message is slowly typed out until the very end, where we are supposed to get our flag. The first thing we should do in any web problem is to inspect the source. Doing so reveals a page called msg.php at the bottom.

Going to [http://162.243.0.171/msg.php](http://162.243.0.171/msg.php) reveals a long string of what looks like hex codes. However, all of the letters a-f have been replaced by the letters o-s. This is simply a ROT-13 cipher applied to hex codes. We canuse a simple online tool such as [this](http://www.rot13.com/) to decrypt it.

Once we have the proper hex codes, we simply need to decode it to get our final message. Doing so reveals the message on the original site, along with the flag

Flag: flag{wa1t1ng_f0r_th3_r3st}


<b> Writeup by Nick DeFilippis </b>
