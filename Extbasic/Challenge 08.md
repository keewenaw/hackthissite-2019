<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/8/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/8start.png" width="500">

Here's the code:
<pre><code>
1   #!/usr/bin/perl
2
3   chomp(my $User = `/usr/bin/whoami`);
4
5   print "Checking your access level...\n";
6
7   if ($User == 'BillGates')
8   {
9     print "Authorized! Here are the company records:\n" . `cat /home/BillGates/CompanyRecords.db`;
10     die("Closing...\n");  
11  }
12
13  die("You're not authorized!\n");
</code></pre>

And interesting lines:

<ul>
  <li>Line 3 sets the variable <code>$User</code> to the output of the command <code>/usr/bin/<a href="http://man7.org/linux/man-pages/man1/whoami.1.html" target="_blank">whoami</a></code>, then removes any line feed characters from the result.</li>
  <li>Line 7 compares <code>$User</code> and the string "BillGates" and executes lines 9 and 10 if the two are the same.</li>
  <li>Line 9 prints out the output of the command <code><a href="http://man7.org/linux/man-pages/man1/cat.1.html" target="_blank">cat</a> /home/BillGates/CompanyRecords.db</code>, as well as some other strings.</li>
</ul>

Some of these lines look interesting. Are we sure that <code>$User</code> isn't empty? Is <code>$User</code> actually a string? Is "BillGates" considered a string? Are we <a href="https://users.cs.cf.ac.uk/Dave.Marshall/PERL/node37.html" target="_blank">comparing</a> <code>$User</code> and "BillGates" appropriately? Why don't you run the script yourself and find out?

When you have your solution, verify it as per normal:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/8success.png" width="500">

Challenge complete.
