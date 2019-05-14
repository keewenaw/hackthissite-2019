<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/9/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/9start.png" width="500">

Reading the little blurb included with this challenge tells us that we'll need to go back to the form in <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/Challenge%2008.md" target="_blank">Challenge 8</a> to figure out this password. Further, the blurb says our SSI attack/solution from before (<code>&#60;!--#exec cmd="ls ../" --&#62;</code>
) put us on the right track here too. So alll we need to do is figure out how to modify our attack to point to our current challenge URL.

Re-reading the <code>ls</code> documentation tells us we can traverse directories in a specific order. Starting from the Challenge 8 form field:
<ul>
  <li><code>ls</code>: <b>/missions/basic/8/tmp/</b></li>
  <li><code>ls ../</code>: <b>/missions/basic/8/</b></li>
  <li><code>ls ../../</code>: <b>/missions/basic/</b></li>
  <li><code>ls ../../9</code>: <b>/missions/basic/9/</b></li>
</ul>

Let's try that as before:

<code>&#60;!--#exec cmd="ls ../../9" --&#62;</code>

And follow the same strategy to uncover and use the password.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/9success.png" width="500">

Challenge complete.
