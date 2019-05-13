<b>Challenge URL:</b> https://www.hackthissite.org/missions/javascript/4/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/4start.png" width="500">

Let's inspect the element and expand the Javascript section.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/4source.png" width="500">

1 <code>RawrRawr = "[your_value]";</code><br>
2 <code>function check(x)</code><br>
3 <code>{</code><br>
4 <code>"+RawrRawr+" == "hack_this_site"</code><br>
5 <code>if (x == ""+RawrRawr+"")</code><br>
6 <code>{</code><br>
7 <code>alert("Rawr! win!");</code><br>
...<br>

If you know the answer from here, feel free to check your result at the bottom of this page. If not, let's figure it out together.

Line 1 is simple, we just set the value of the variable <code>RawrRawr</code> to the value in double quotes. 

Line 4 is the trickiest line. You may think we're changing the value of <code>RawrRawr</code> again, but look closely. There are two equal signs instead of one. One equal sign means we're setting a variable, two mean we're comparing two values (<a href="https://www.w3schools.com/js/js_operators.asp" target="_blank">source</a>). So Line 4 is verifying if the strings "+RawrRawr+" and "hack_this_site" are the same string. They're not, so this evaluates to "false". You can verify this by running Line 4 through the Javascript interpreter of your choice. We don't do anything with this result, so can safely ignore the line.

Line 5, we know is comparing our input to the form, <code>x</code>, to the value contained in <code>""+RawrRawr+""</code>. Let's examine the second clause, because yet again, all is not as it seems. Two double quotes next to each other indicate a <code>null</code> string. The plus sign actually is the <a href="https://www.w3schools.com/js/js_operators.asp" target="_blank">string concatenation operator</a>. So this line actually compares <code>x</code> to the total of (the <code>null</code> string, concatenated with our value for <code>RawrRawr</code>, concatenated with the <code>null</code> string again). Basically, whatever <code>RawrRawr</code> gets set to in Line 1 is our password! Let's verify by inputting it into the challenge's form field.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/4success.png" width="500">

Challenge complete!
