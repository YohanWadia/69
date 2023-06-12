# Step 5
<h2>Handling Logical Oversight</h2>
<pre>
eg. if we have 12344 as a number
when we extract the last digit 4... and save it to the array... 
the array will look like [0][0][0][0][4][0][0][0][0][0]
and the number is reduced to 1234

But now there is another 4!?
At this time we need an if condition that checks
if the box with index no.4 already has a value of 4 stored in it...
that means this new digit, is a duplicate.
Hence this number fails the test... it must break the loop 



We need to declare an array of type int with a space of 10 boxes
so by default it will look something like this [0][0][0][0][0][0][0][0][0][0]
ONLY the perfect number will fill the array up like this [0][1][2][3][4][5][6][7][8][9]... SINCE IT WILL HAVE ALL 10 DIGITS
any other number that has a repeating digit must FAIL & the loop should break since it doesnt
satisfy the solution for the problem.

So on every digit extaction save that digit to its own box.
Like if you extracted digit 5... then array[5]=5; 
And now the value of 5 has been saved to the array's box 5(index)
if you extracted digit 9... then array[9]=9; 
And now the value of 9 has been saved to the array's box 9(index)

### <b>Example<b> ======================================
 Say the number is 8795460123. (has all 10 digits)
 this is what should happen when you loop 10 times
