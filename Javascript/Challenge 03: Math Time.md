<b>Challenge URL:</b> https://www.hackthissite.org/missions/javascript/3/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/3start.png" width="500">

Thankfully, we're given the source code up front, so let's highlight the relevant lines below:

...<br>
2 <code>var foo = 5 + 6 * 7</code><br>
3 <code>var bar = foo % 8</code><br>
4 <code>var moo = bar * 2</code><br>
...<br>
8 <code>if (x.length == moo)</code><br>
...<br>
10 <code>alert("win!");</code><br>
...<br>

If you know how to read and evaluate this code, feel free to skip to the end and see if you get the same win condition. If not, read on!

Let's start with lines 8 and 10. Basically, we take the value of <code>x</code> (whatever we input into the text box) and get  <code>x</code> 's length/amount of characters in <code>x</code>. Eg, an input of "test" will return 4, since "test" has four characters. If the length of our input is equal to the value of the variable <code>moo</code>, we'll beat the challenge. 

Now what is the value of <code>moo</code>? Let's look at lines 2-4 to figure it out. 

We start by trying to calculate the value of <code>foo</code>. Given the <a href="https://www.sitepoint.com/javascript-operators-conditionals-functions/#operatorprecedence" target="_blank">Javascript order of operations</a>, we know that we evaluate the <code>6 * 7</code> part first, then add five. So 6 * 7 = 42, 42 + 5 = 47. Our value for <code>foo</code> is 47.

For <code>bar</code>, we'll take <code>foo % 8</code>. The percent sign is known as the "<a href='https://www.sitepoint.com/javascript-operators-conditionals-functions/#modulus' target='_blank'>modulus</a>" operator, and will return the remainder of a division operation instead of the quotient. Eg, <code>5 / 2</code> will yield 2 remainder 1. 2 is our quotient and 1 is our remainder, so <code>5 % 2</code> returns 1. In line 3, <code>foo % 8</code> is equivalent to <code>47 % 8</code>. 47 divided by 8 is 5 remainder 7. Ergo, <code>bar</code> gets set to 7.

For <code>moo</code>, <code>moo</code> gets set to <code>bar * 2</code>. Since <code>bar</code> is 7, seven times two is 14. Hence, <code>moo</code> is 14.

Taking that, line 8 changes to <code>if (x.length == 14)</code>. All we need to do is input a string with length 14, and we should win.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Javascript/screenshots/3success.png" width="500">

Challenge complete!
