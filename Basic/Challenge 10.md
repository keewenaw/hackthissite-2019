<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/10/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/10start.png" width="500">

And reading the challenge information snippet tells us:

<blockquote>This time Sam used a more temporary and "hidden" approach to authenticating users, but he didn't think about whether or not those users knew their way around javascript...</blockquote>

The first thing that fits this explanation are <a href="https://www.w3schools.com/js/js_cookies.asp" target="_blank">cookies</a>. Let's immediately examine our currently-set cookie via the Firefox developer console. To access that, press the <code>Control+Shift+K</code> keys simultaneously. Then we can type in the string <code>document.cookie</code> to see the contents of the currently-set cookie.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/10cookiebase.png" width="500">

Well, I certainly hope I don't need to explain why this field matters! Let's try setting <code>level10_authorized</code> manually to "yes" by inputting the following into the console:

<code>document.cookie="level10_authorized=yes; PHPSESSID=[your_PHPSESSID]"</code>

We can verify this took by re-doing our <code>document.cookie</code> command and verifying the output changes as expected. We can then put a random string in the password field, and then clicking the "submit" button.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/10success.png" width="500">

There we go! Challenge complete.
