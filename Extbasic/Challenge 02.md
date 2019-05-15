<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/2/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/2start.png" width="500">

Here's the code:
<pre><code>
1 &#60;php
2 $lvl_text = file_get_contents($_POST['filename'].'.php');
3 ?&#62;
</code></pre>

<ul>
  <li>Lines 1 and 3 just indicate that this is a PHP program and can safely be ignored in this instance.</li>
  <li>Line 2 gets the HTTP POSTed value called <code>filename</code>, then tries to load the contents of <code>[filename].php</code> into the variable <code>$lvl_text</code>.</li>
</ul>

We know our target is a PHP file based on the description, so we don't need to specify any file extension as one will automtically be added. 

Your first thought may be to try something like "index", since we want <code>$lvl_text</code> to store the source code for <b>index.php</b>. But look closely at the URL. We aren't in the same directory as the target, are we? 

Also note that the program doesn't filter or sanitize the value of <code>filename</code> before using it. I wonder what we could do with that? <a href="https://www.owasp.org/index.php/Testing_for_Local_File_Inclusion" target="_blank">This link</a> may be worth looking at.

When you find the solution, input it into the form:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/2success.png" width="500">

Challenge complete!
