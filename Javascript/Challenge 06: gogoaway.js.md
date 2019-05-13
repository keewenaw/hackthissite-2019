<b>Challenge URL:</b> https://www.hackthissite.org/missions/javascript/6/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/6start.png" width="500">

Well that doesn't sound good! Let's inspect the element:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/6source1.png" width="500">

We can see a reference to a new Javascript file, <b>/missions/javascript/6/checkpass.js</b>, near the top of our screenshot. Let's open that file up and see what we find:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/6source2.png" width="500">

If we remember how <a href="https://www.w3schools.com/js/js_operators.asp" target="_blank">string concatenation</a> works in Javasript, we can see that the password is "[your_string3] [your_string2]", with a space between the two values. Get your two values, assemble them in the right order, add a space, and ...

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/6success.png" width="500">

Voila, challenge complete!
