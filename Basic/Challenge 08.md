<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/8/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/8start.png" width="500">

Let's test this new program by inputting the text "test" into the upper form field. We first get a notification that a new file was created:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/8test1.png" width="500">

When we click the hyperlink, we see this: 

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/8test2.png" width="500">

It seems to output our initial test string, then tells us how many characters were in that string.

This looks similar to <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/Challenge%2007.md" target="_blank">our last challenge</a>, so our strategy will be similar. However, since this is a PHP script, not Perl, we'll need to find a way to execute a command within PHP proper. Pentesters call this kind of attack a "<a href="https://www.owasp.org/index.php/Server-Side_Includes_(SSI)_Injection" target="_blank">Server-Side Includes Injection</a>", or SSI for short. To do so, we execute something like:

<code>&#60;!--#exec cmd="ls" --&#62;</code>

Let's try that now:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/8exec.png" width="500">

Okay, great, we're on the right track. We didn't get the right answer though - if we look at the URL, we are actually a directory directories below the password file. We're in <b>8/tmp/</b>, so we need to move up one directory and list the contents there. To do so, we'd modify our command as follows:

<code>&#60;!--#exec cmd="ls ../" --&#62;</code>

Running this gives us another directory listing, and we see a few files that tell us we're in the right place (index.php being one). We'll see another file with an apparently random name, so let's visit that. We'll see our password as before. Input it in the form field, and we should be good to go.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/8success.png" width="500">

Challenge complete.

