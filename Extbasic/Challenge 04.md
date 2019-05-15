<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/4/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/4start.png" width="500">

Here's the code:
<pre><code>
1 BEGIN F.ake
2 var int as in
3 int var as in
4 out var int
</code></pre>

We're dealing with obfuscated code again, and the obfuscation seems to work very similar to <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/Challenge%2003.md" target="_blank">Challenge 3</a>.

<ul>
  <li>Line 1 defines a program called "F" with an extension of "ake".</li>
  <li>Line 2 defines a variable called <code>var</code>, an integer, with a value of "in".</li>
  <li>Line 3 defines a variable called <code>int</code>, a variable, with a value of "in".</li>
  <li>Line 5 outputs the values of <code>var</code> and <code>int</code> in some manner.</li>
</ul>

We also see a small note right above the code snippet, which states "{user types 6,7}". That tells us "in" must be referring to user input. We now know what <code>var</code> and <code>int</code> get defined as, so the only issue becomes how these values get modified and/or displayed to the user.

Once you figure out the formatting, input your solution:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/4success.png" width="500">

Challenge complete!
