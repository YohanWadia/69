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
 
 for(int i = the starting number; i< the ending number; i increment by 1 ) {

int sq = the square of the number  i is atm
int cube = the cube of the number  i is atm

//you might also be asked by intelliJ to cast the below line to long
long num = (cube * X) + sq; // X stands for 10? or 100? or 1000? or 10000?

declare an array of 10 boxes
initialize the value at index 0 to -1

 for( int j = start with 0;  ends at <10; increment by 1){
 int digit = (int)(num%10); // casting the remainder(hence getting the last digit)
 num = num/10; //reducing the number
  if(the value at array[digit] is equal to the digit){
   means this digit was already saved, its a duplicate, just break the loop
  }
  else{
   means all good we can save digit to the box at array[digit] 
 }
 
 //Now the if condition that gives us the final answer
  if(j is equal to 9){
   means we have reached all the way till the 10th digit
   and the loop never broke. Hence all the 10 numbers never broke
   the loop. That means this number satisfied all the criterias.
   System.out.println("The answer: " + i);
  }
  
 }//ending bracket for J loop
 
}//ending bracket for I loop






</pre>
