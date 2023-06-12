# Step 3
<h2>Breaking the large number into its digits</h2>
<pre>
After getting the large number that is a join of the square and cube, We will need to test its digits.
For this we will need to get each digit individually to check that they havent repeated... and that means all the
10 digits from 0-9 will be there!

### <b>Example<b> ======================================
 Say the number is 5102587.
 we will need to extract 7 from 5102587.
 next
 we will need to extract 8 from what is left in 510258.
 next
 we will need to extract 5 from what is left in 51025.
 next
 we will need to extract 2 from what is left in 5102.
 next
 we will need to extract 0 from what is left in 510.
 next
 we will need to extract 1 from what is left in 51.
 next
 we will need to extract 5 from what is left in 5.
 
We can save all these digits we extracted to an array with 10 boxes.  
it might look something like this
[0][1][2][][][5][][7][8][]
NOTICE... we have only filled in those digits which exist in the number.
In the perfect number... all 10 boxes will be filled up from 0 - 9.
Hence no digit must repeat.
 
but this particular number fails since 5 does repeat...and all the boxes
of the array havent been filled up.


### <b>Digit Extraction<b> ======================================
Hint: what does this code do?

Eg.1
long num = 12565102587L;//a long data type
int digit = (int)(num%10); // casting the remainder(hence getting the last digit)
num = num/10; //division(hence dropping the last digit from the number) 
System.out.println(digit);
System.out.println(num);

Eg.2
long num = 12345L;
int digit = (int)(num%10);
num = num/10;
System.out.println(digit);
System.out.println(num);

Do you notice the extraction of the last digit & the reduction of the number



### <b>ALL Digit Extraction<b> ======================================
What if you put Eg.2 code into a forloop that runs 5 times?
Hint: start it at '0'... and end it at '<5'

  
  
If you have successfully understood the extraction you can proceed...  















