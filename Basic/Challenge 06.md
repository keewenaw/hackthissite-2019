<b>Challenge URL:</b> https://www.hackthissite.org/missions/basic/6/
<br><br>
<i>Did you remember to read this section's <a href="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/README.md">README</a>?</i>

<h2><b>The Guide</b></h2>

When we start the challenge, here's what we see:

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/6start.png" width="500">

They made life really easy for us here. Not only did they give us the encrypted password, "67:6eggi", but they also gave us a way to discover the algorithm to decrypt it. Let's try this with sample text: <code>aaaaaaaa</code>. When we click "encrypt", our result is <code>abcdefgh</code>. 

With that, we can see the algorithm works by incrementing a counter, then changing the character by adding the numeric value of the character to the counter value. Eg:
<ol type="1">
  <li>The first character is "a" and the counter is 0, so the output letter becomes "a".</li>
  <li>The second character is "a" and the counter is 1, so we "move up" one on the ASCII table to return "b".</li>
  <li>The third character is "a" and the counter is 2, so moving the third character up two returns "c".</li>
  <li>This repeats until the end of the string.</li>
</ol>

So in order to decrypt a ciphertext like the one the challenge gave us, we should take each character and <i>subtract</i>, not add, the counter to get the plaintext.

That probably didn't make too much sense, so I created a simple Python script to do the decryption for us:

<pre><code>
#!/usr/bin/python
# Our ciphertext
ciphertext="[REPLACE_ME]"
# Get the length of the ciphertext
ciphertext_length = len(ciphertext)
# Our plaintext after we decrypt "ciphertext"
result=""

# For all characters in the "ciphertext" string value ...
for i in range(0,ciphertext_length):
	# Get the character at position i
	char = ciphertext[i:i+1]
	# Convert it to an integer
	char_value = ord(char)
	# Modify it as per the algorithm
	char_value = char_value - i
	# Convert it back to a character and add it to our result
	result = result + chr(char_value)

# Show us the result
print result
</code></pre>
  
Run the script with your ciphertext, and input the result into the input field.

<img src="https://github.com/keewenaw/hackthissite-2019/blob/master/Basic/screenshots/6success.png" width="500">

Challenge complete!
