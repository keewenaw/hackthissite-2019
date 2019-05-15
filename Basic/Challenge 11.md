<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/11/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/11start.png" width="500">

That really doesn't tell us much. Pretty disappointing. Let's view the page source to see if we find anything useful.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/11source.png" width="500">

Awesome, so we see there's a private music collection somewhere. That tells us there's a hidden directory we need to find. 

If we refresh the page, we see that the (what I'm guessing are) song names vary on each refresh. A few I've gotten include:
<ul>
  <li>"The Cage"</li>
  <li>"Amoreena"</li>
  <li>"The Captain and the Kid"</li>
  <li>"From Denver to L.A."</li>
</ul>

We can look up a few of those song names and find the artist who recorded them (I won't tell you who). Now comes the question of how to use this information and find the hidden directory. Why not try creating a list of possible variants of the artist's name and try loading that into a tool like "Dirbuster", see if we can find it that way? Or heck, brute force it yourself (I promise it's not too hard. Just start small!). You'll know you're on the right track when you see a page with "Index of [directory]" as the header.

Regardless of how you find it, navigate to the end. You'll see nothing at all ... or so we think. We know the challenge uses Apache, and if you have prior Linux experience, we know there are certain ways to mask files from appearing in directory listings. Those files are called "hidden files", and a very common one for Apache is <b>.htaccess</b>. Since it sounds the developer didn't protect his Apache install correctly, let's try visiting that file now. 

Let's look at the first line: <code>IndexIgnore [a_file_name].* .htaccess</code>. We'll need to figure out what extension this file is, so let's start by just visiting that filename in our browser without an extension specified. Surprisingly, it works! We get a two-line message. The contents of the message are vital to discovering the password. I'll only say this: abstract thinking isn't an asset for this riddle.

Now we'll need to find the password prompt. Normally, in these circumstances, the root page for a given directory is an index, something like <b>index.php</b> or <b>index.html</b>. So if we start there, starting at the root <b>/basic/11/</b> directory, we'll find the following URL: <b>/missions/basic/11/index.php</b>

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/11pwprompt.png" width="500">

Let's input our password here:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/11success.png" width="500">

The final completion message differs from the rest, but retrying the challenge will verify you've completed it. Challenge complete!
