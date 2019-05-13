<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/1/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1start.png" width="500">

When beginning a penetration test of a web-based application, I start by inspecting the source code. When the web app is very simple, having only a few elements, I prefer using "Inspect Element" to view each code snippet separately. You can do that by right-clicking on the element you want to examine, then selecting the "Inspect Element" option.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1source.png" width="500">

Wow! They give us the password right there, just from reviewing the source code. It's in a comment block, which you can tell by the <code>&#60;!--</code> and <code>--&#62;</code> delimiters.

Let's check to see if it works.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1success.png" width="500">

Success, it does! Challenge complete.
