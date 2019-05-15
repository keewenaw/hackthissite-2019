<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/7/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/7start.png" width="500">

Here's the relevant code:
<pre><code>
1   &#60;?php
2   if (!empty($_POST['data']))
3   {
4       $data = mysql_real_escape_string($_POST['data']);
5       mysql_query("INSERT INTO tbl_data (data) VALUES ('$data')");
6   }
7   ?&#62;
8   &#60;form name="grezvahfvfnjuvavatovgpu" action="&#60;?=$_SERVER['PHP_SELF']?&#62;" method="get"&#62;
9   &#60;input type="text" name="data" /&#62;
10  &#60;input type="submit" /&#62;
11  &#60;/form&#62;
</code></pre>

A code summary of the noteworthy parts is below:

<ul>
  <li>Line 3 takes the POSTed <code>data</code> field, tries to sanitize it, and stores it in the <code>$data</code> variable.</li>
  <li>Line 4 builds a MySQL query using the sanitized variable from line 3 and executes it.</li>
  <li>Line 8 specifies the form name, an action to take upon submitting the form (a PHP code snippet that calls <code>$_SERVER['PHP_SELF']</code>), and the HTTP request type.</li>
</ul>

Let's look at line 8 and start with the bug. What request type do we specify? Is that the same kind we use? if so, why? If not, why not?

For the action, the <code>$_SERVER['PHP_SELF']</code> line returns the filename of the currently running script (<a href="https://www.w3schools.com/php/php_form_validation.asp" target="_blank">source</a>). The developer probably expects a standard filename like "index.php". What if it's not "normal"? What if the attacker wants to add special characters, like a <code>&#60;script&#62;</code> tag? Can we <a href="https://www.php.net/manual/en/filter.filters.sanitize.php" target="_blank">protect against that</a>?

If you think you've got it, go ahead and check:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/7success.png" width="500">

Challenge complete.
