# Step 5
<h2>Handling Logical Oversight</h2>
<pre>
eg. if we have 12344 as a number
when we extract the last digit 4... and save it to the array... 
the array will look like [0][0][0][0][4][0][0][0][0][0]
and the number is reduced to 1234

**But now there is another 4!?**
At this time we need an if condition that checks
if the box with index no.4 already has a value of 4 stored in it...
that means this new digit, is a duplicate.
Hence this number fails the test... it must break the loop 

**Problem with 0**
Incase the digit you are going to save to the array is 0
then the above if condition will fail... because
the value at index 0 is already having a default value ie = 0.
At this time the digit being saved(0) is being checked with
the value in box [0] which is also 0... and hence it will think
we are saving a duplicate! hence after we make the array we have to
initialize array[0] to another numbere.. eg. array[0] = -1;

### <b>Final Pseudo code should be something like this<b> ======================================
 





</pre>
