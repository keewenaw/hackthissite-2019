<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/3/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/3start.png" width="500">

Here's the code:
<pre><code>
1 BEGIN notr.eal
2 CREATE int AS 2
3 DESTROY int AS 0
4 ANS var AS Create + TO
5 out TO
</code></pre>

Since this code is obfuscated, our logical best guess for what this program does is below:

<ul>
  <li>Line 1 defines a program called "notr" with an extension of "eal"</li>
  <li>Line 2 defines a variable called <code>CREATE</code>, an integer, with value 2.</li>
  <li>Line 3 defines a variable called <code>DESTROY</code>, an integer, with value 0.</li>
  <li>Line 4 is the trickiest, but seems to evaluate the value of <code>CREATE</code> added to <code>TO</code>, storing the result in the varlable <code>ANS</code>.</li>
  <li>Line 5 outputs the value of <code>TO</code>.</li>
</ul>

Hm, it seems <code>TO</code> doesn't get explicitly defined - I wonder what the default value of a newly-initialized variable would be here? However, we see that <code>CREATE</code> and <code>DESTROY</code> get set to 2 and 0 respectively. I wonder if one of those values play into it? <code>CREATE</code> certainly does. I also can't help but wonder what the <code>+</code> actually does. Maybe it doesn't actually mean the mathematical operator? Makes you think ...

When you think you have the final value of <code>TO</code>, try submitting it in the form field:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/3success.png" width="500">

Challenge complete!
