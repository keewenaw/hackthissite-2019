<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/1/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/1start.png" width="500">

Here's the code:
<pre><code>
1 void blah(char *str)
2 {
3   char lol[200];
4   strcpy(lol, str);
5 }
</code></pre>

There are only five lines here, so code analysis shouldn't cause us too much trouble.

<ul>
  <li>Line 1 defines a function <code>blah</code>, which takes a single argument, <code>*str</code>. <code>*str</code> is a string, which in C manifests as an array of characters.</li>
  <li>Lines 2 and 5 only indicate where the function code begins and ends, so don't really matter in this context.</li>
  <li>Line 3 is a variable definition, which defines <code>lol</code> as an empty array with two hundred spaces.</li>
  <li>Line 4 copies whatever value is in <code>*str</code> into the two hundred spaces in <code>lol</code>.</li>
</ul>

Essentially, here's the issue - we know we have two hundred spaces that we can fill in <code>lol</code>. What happens when we try to fit something other than two hundred characters into that space? What if <code>*str</code> has a length of 10 characters, or 100, or 1000? <a href="https://www.veracode.com/security/buffer-overflow" target="_blank">Here</a> is a good link to reference when trying to solve this challenge. 

When you have it, you'll see a blue "Go on" button, like so:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/1success.png" width="500">

Click it to complete the challenge!
