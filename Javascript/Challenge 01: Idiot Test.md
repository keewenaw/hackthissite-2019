<b>Challenge URL:</b> https://www.hackthissite.org/missions/javascript/1/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/1start.png width="500">

When beginning a penetration test of a web-based application, I start by inspecting the source code. When the web app is very simple, having only a few elements, I prefer using "Inspect Element" to view each code snippet separately. You can do that by right-clicking on the element you want to examine, then selecting the "Inspect Element" option.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/1source.png" width="500">

If we look near the top, we see a grey compacted line:

<code>&#60;script language="Javascript"&#62;...&#60;/script&#62;</code>

Let's expand that out ...

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/1javascript.png" width="500">

... and as soon as we do, we see the password! There's no encryption, obfuscation, or anything. As a pentester, I love it when that happens. As a user of a site? Not so much. Let's go back to the challenge form and input the found string:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/1success.png" width="500">

Challenge complete!
