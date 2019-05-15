<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/5/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/5start.png" width="500">

Here's the relevant code:
<pre><code>
1 #!/bin/sh
2 rm OK
3 sed -E "s/eval/safeeval/" &#60;exec.php &#62;tmp && touch OK
4 if [ -f OK ]; then
5        rm exec.php && mv tmp exec.php
6 fi
</code></pre>

A code summary is below:

<ul>
  <li>Line 1 is normal for shell scripts; it points the script to the specific shell executable to run this program with (there are quite a few).</li>
  <li>Line 2 removes the file or object "OK".</li>
  <li>Line 3 replaces instance(s) of the string "eval" in the file <code>exec.php</code> with "safeeval" and stores the result in <code>tmp</code>. Further, this creates a new, empty file called "OK".</li>
  <li>Line 4 says if the file <code>OK</code> exists, execute line 5.</li>
  <li>Line 5 removes the file <code>exec.php</code> and renames the temporary file <code>tmp</code> to <code>exec.php</code>.</li>
  <li>Line 6 closes out the "if" statement from line 4.</li>
</ul>

To solve this, let's look at the core code, line 3. <a href="https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/" target="_blank">Here</a>'s the documentation on <code>sed</code>; I'd look very closely at it. What does the <code>-E</code> flag do? What does <code>s/eval/safeeval/</code> do? Does it do what we think it should in all instances, or only some of them?

Once you have it, input the line into the form field to verify:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/5success.png" width="500">

Challenge complete.
