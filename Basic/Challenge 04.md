<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/4/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/4start.png" width="500">

And if we inspect the element:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/4source.png" width="500">

We can see that the dev severely messed up with how the script works. The dev pulls information from the client-side without a good reason - the email the script sends the password to is specified as a hidden field. That's huge! If we can change the listed email to one we control, we should get the password reminder ourselves. So in the "Inspector" window, change the email to one of your emails. Click outside of that line of code to "commit" your change, then click the "Send password to Sam" button.

You should get a notification like this:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/4password.png" width="500">

And if you check your email, you should get an email with the subject line "Your password reminder" from the sender "sam@hackthissite.org". Take the discovered password and input it into the original form field, and you should be set:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/4success.png" width="500">

Challenge complete!
