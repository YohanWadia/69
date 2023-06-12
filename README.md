# Step 4
<h2>Saving to the Array</h2>
<pre>
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
 
 when i=0 in the loop:
 the extracted digit is 3
 and the number is reduced to 879546012
 and the array looks like this [0][0][0][3][0][0][0][0][0][0] 
 
 when i=1 in the loop:
 the extracted digit is 2
 and the number is reduced to 87954601
 and the array looks like this [0][0][2][3][0][0][0][0][0][0]
 
 when i=2 in the loop:
 the extracted digit is 1
 and the number is reduced to 8795460
 and the array looks like this [0][1][2][3][0][0][0][0][0][0]
 
 when i=3 in the loop:
 the extracted digit is 0
 and the number is reduced to 879546
  and the array looks like this [0][1][2][3][0][0][0][0][0][0]
 
 when i=4 in the loop:
 the extracted digit is 6 
 and the number is reduced to 87954
  and the array looks like this [0][1][2][3][0][0][6][0][0][0]
 
 when i=5 in the loop:
 the extracted digit is 4
 and the number is reduced to 8795
  and the array looks like this [0][1][2][3][4][0][6][0][0][0]
 
 when i=6 in the loop:
 the extracted digit is 5
 and the number is reduced to 879
   and the array looks like this [0][1][2][3][4][5][6][0][0][0]
 
 when i=7 in the loop:
 the extracted digit is 9
 and the number is reduced to 87
   and the array looks like this [0][1][2][3][4][5][6][0][0][9]
 
 when i=8 in the loop:
 the extracted digit is 7 
 and the number is reduced to 8
 and the array looks like this [0][1][2][3][4][5][6][7][0][9]

 when i=9(THE LAST STEP) in the loop:
 the extracted digit is 8
 and NO DIGITS ARE LEFT IN THE NUMBER
 THE FULLY FILLED ARRAY  [0][1][2][3][4][5][6][7][8][9]
 
 
 ### <b>PSEUDO CODE<b> ======================================
 
 declare an array of 10 boxes
 forloop(from 0 till <10){
  //extract digit & reshape num from eg.2 in Step3
  int digit = (int)(num%10);
  num = num/10;
  
  save the digit to its own box in the array  
 
 }
 
 
 
 
 
 
 
 
 
