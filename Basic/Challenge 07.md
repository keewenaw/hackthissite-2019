<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/7/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/7start.png" width="500">

Let's test the calendar script by inputting the current year, "2019".

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/7test.png" width="500">

It appears that the form takes user input and adds it as a parameter to some sort of command (given the output, the Linux "<code><a href="http://man7.org/linux/man-pages/man1/cal.1.html" target="_blank">cal</a></code>" command seems likely). It then outputs the result of the command. No sanitization of the input or output appears to take place, given that we don't see any headers or formatting that looks custom. Further, we can input invalid years like "asdf" and cause an expected error (no output at all).

We usually attack programs like this by first attempting to chain commands together. I actually discussed the basics of command chaining in my <a href="https://github.com/keewenaw/dvwa-guide-2019/blob/master/low/Challenge%2002:%20Command%20Injection.md" target="_blank">one of my DVWA writeups</a>, so I won't rehash the explanation here. Feel free to review the linked article if you want more details. The salient point is to use the <code>;</code> character to combine two commands.

Okay, so we know the following:
<ol type="a">
  <li>We need to insert a valid year to see any output;</li>
  <li>We can chain commands together with <code>;</code>; and</li>
  <li>We can find the password file in our current working directory, but we don't know the exact name.</li>
</ol>

Thankfully for us, we know of a Linux command that lists all files in a given directory. That's "<code><a href="http://man7.org/linux/man-pages/man1/ls.1.html" target="_blank">ls</a></code>"! We don't immediately see a reason this couldn't work, so let's build an attack string as follows:

<code>2019; ls</code>

And if we input that string into the form and view the result, we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/7cmd.png" width="500">

Right underneath where my screenshot ends, you'll find a PHP file with a random string as a filename. Visit that file in your browser, and you'll see another random string, which the challenge tells us is our password. Input it into the form field, and ...

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/7success.png" width="500">

Challenge complete!
