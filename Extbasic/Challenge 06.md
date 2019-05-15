<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/6/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/6start.png" width="500">

Here's the code:
<pre><code>
1   &#60;?php
2     $user = $_GET['user'];
3     $pass = $_GET['pass'];
4     if (isAuthed($user,$pass))
5     {
6       $passed=TRUE;
7     }
8     if ($passed==TRUE)
9     {
10      echo 'you win';
11    }
12  ?&#62;
13  &#60;form action="me.php" method="get"&#62;
14  &#60;input type="text" name="user" /&#62;
15  &#60;input type="password" name="pass" /&#62;
16  &#60;/form&#62;
17  &#60;?php
18    function isAuthed($a,$b)
19    {
20      return FALSE;
21    }
22  ?&#62;
</code></pre>

Most lines don't matter for our purposes, so here are the relevant ones:

<ul>
  <li>Line 2 gets the user input (assumedly a username) from the HTTP GET request and stores it in the variable <code>$user</code>.</li>
  <li>Line 3 gets the user input (assumedly a password) from the HTTP GET request and stores it in the variable <code>$pass</code>.</li>
  <li>Line 4 checks to see if we're authenticated. If so, line 6 will set the variable <code>$passed</code> to <code>TRUE</code>.</li>
  <li>Line 8 checks if <code>$passed</code> is set to <code>TRUE</code>. If it is, we win.</li>
  <li>Line 18 is the authentication function. It always returns <code>FALSE</code>.</li>
</ul>

As-is, we'll never be authenticated! How can we make <code>$passed</code> <code>TRUE</code> if <code>isAuthed()</code> always returns <code>FALSE</code>? Do you think we can find a way to set <code>$passed</code> "manually", just like we did with the <code>user</code> and <code>pass</code> GET fields? Review the basics of <a href="https://www.w3schools.com/tags/ref_httpmethods.asp" target="_blank">HTTP GET requests</a> if you need to. Give it a shot!

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/6success.png" width="500">

Challenge complete!
