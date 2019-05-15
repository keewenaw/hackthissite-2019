<b>Challenge URL:</b> https://www.hackthissite.org/missions/extbasic/9/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/9start.png" width="500">

Here's the code, slightly cleaned up:
<pre><code>
1   #!/usr/bin/perl
2   print '&#62; Hello Captain ' . $ENV{'USER'} . '.' . "\n";
3   open(STARTREKLOG, '&#62;/var/log/startrek');
4   print '&#62; Please enter your log data here, end with a "." on a single line.' . "\n";
5   my $LogText;
6   print '&#62; ';
7   while (&#60;STDIN&#62;) {
8     unless ($_ ne '.' . "\n") {
9       last;
10    }
11    $LogText .= $_;
12    print '&#62; ';
13    }
14
15    print '&#62; Log is being saved to /var/log/startrek' . "\n";
16    $DateTime = localtime();
17    print STARTREKLOG ' -- START OF LOG -- ' . "\n";
18    print STARTREKLOG 'Date/Time: ' . $DateTime . "\n";
19    print STARTREKLOG 'Log      : ' . $LogText;
20    print STARTREKLOG ' -- END OF LOG -- ' . "\n";
21    die('&#62; Log saved! Now exiting.' . "\n");
</code></pre>

Let's look at the interesting lines:

<ul>
  <li>Line 2 echoes some text, but also pulls in the <a href="https://perldoc.perl.org/Env.html" target="_blank"> environment variable</a> <code>USER</code>.</li>
  <li>Line 3 <a href=https://perldoc.perl.org/functions/open.html" target="_blank">opens a file</a> called <code>STARTREKLOG</code> at the location <b>/var/log/startrek</b>.</li>
  <li>Line 7 will continuously loop as long as there's text being input by the user. When the input indicates we should end, the loop "breaks" (ends).</li>
  <li>Lines 17-20 all write data to our new file.</li>
</ul>

Since the challenge tells us the problem (each use of this script overwrites all the old logs), we know the issue is contained to lines that modify our log file. 

Try and see if you can answer the following questions on your own. Are we opening up the file correctly? Do we have the right parameters for opening files? Are they defined appropriately? Are the values we're passing as parameters correct? Are we writing to the right file and location? Can we corrupt the file based on the data we write to it? The links I provided in the code summary may help you answer.

When you're ready, validate as before.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Extbasic/screenshots/9success.png" width="500">

Challenge complete.
