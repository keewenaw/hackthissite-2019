<b>Challenge URL:</b> https://www.hackthissite.org/missions/javascript/5/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/5start.png" width="500">

I have no idea what the Runescape message has to do with anything, so let's just inspect the element as per normal.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/5source.png" width="500">

We see a very interesting line, <code>moo = unescape('[your_value]');</code>. We then can see if we decode the value of <code>moo</code> and input it into the challenge's field. You can do this manually (it's just hex-encoded). Or you can easily do this by taking the entire line, then opening the Firefox developer console by pressing the <code>Control+Shift+K</code> keys simultaneously. We then can copy and execute the line of code. If we type <code>moo</code> again, we can see the expected password.

Regardless of how we find the password, let's see if it works.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/5success1.png" width="500">

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/5success2.png" width="500">

Challenge complete!
