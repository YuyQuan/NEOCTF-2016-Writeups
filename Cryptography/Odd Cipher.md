<b>Problem:</b><br>
nukr{JAxhUWVEkdJp}<br>
Need to mention, there are numbers in the flag, and also, there is an underscore in the 11th character of the flag. Shoutout to 
team n0de for solving this problem without this information somehow :).<br>
Hint: Should come out to be a readable phrase<br><br>
<b>Solution:</b><br>
Ok, so this is an odd cipher. If you observe how the first 4 characters relate to flag, you'll notice that the shifting increment increases by 1 every time. How odd.<br>
Of course, what's odder is that sometimes the letters will shift back to the beginning of their corresponding upper or lowercase alphabet, or they'll shift to a number of underscore.<br>
To fix that, just edit the program below [whether or not it cycles] and find the readable combination of the outputs. Voila.<br><br>
def shift(n,s):<br>
```python
&nbsp;&nbsp;&nbsp;&nbsp;if ord(n) > 96 and ord(n) - s < 97:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return chr(ord(n)-s+26)<br>
&nbsp;&nbsp;&nbsp;&nbsp;elif ord(n) > 64 and ord(n) - s < 48:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return chr(ord(n)-s+26)<br>
&nbsp;&nbsp;&nbsp;&nbsp;return chr(ord(n)-s)<br>
flag = 'nukr{JAxhUWVEkdJp}'<br>
message = ''<br>
step = 8<br>
for char in flag:<br>
&nbsp;&nbsp;&nbsp;&nbsp;message += shift(char,step)<br>
&nbsp;&nbsp;&nbsp;&nbsp;step += 1<br>
print(message)
```<br><br>
flag: flag{W3irD_C1ph3r}<br>
<b>by defund [team n0de]</b><br>
Note: This is the sort of challenge where you can't think that much while solving it; I did it half asleep on the schoolbus.

