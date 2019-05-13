<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/1/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1start.png" width="500">

When beginning a penetration test of a web-based application, I start by inspecting the source code. When the web app is very simple, having only a few elements, I prefer using "Inspect Element" to view each code snippet separately. You can do that by right-clicking on the element you want to examine, then selecting the "Inspect Element" option.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1source.png" width="500">

Wow! They give us the password right there, just from reviewing the source code. It's in a comment block, which you can tell by the <code>&#60;!--</code> and <code>--&#62;</code> delimiters.

Let's check to see if it works.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/1success.png" width="500">

Success, it does! Challenge complete.

<i>As an aside, I can verify things like this do happen in the real world. Back in grad school, I freelanced as an independent IT security consultant. No, that's not a euphemism, I had legal contracts and everything. One of my engagements was to break into a private forum; think something similar to phpBB. When I discovered the administrator section, I looked at the source code as per normal. All the way at the bottom of the page, they included a set of credentials in a comment. Only reason I noticed was because I saw the scroll bar on the bottom of my browser seemed much longer than the page source code would indicate. I logged in with them, only to discover the creds were for an admin-level account! Total time to compromise, about 8 minutes. Easiest paycheck I ever made.</i>
