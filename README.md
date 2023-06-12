# Step 2
<h2>Number Concatenation</h2>
<pre>
After getting the number we are on(atm in the for loop via <b>i</b>) we have saved its square and cube to 2 separate int variables.

Now we need to join them.. ie concatenate them. And in doing so we will observe all the digits 0123456789. 
Please note there can be no repeat of a digit... if there is a digit that repeats for eg 012344456789 .. it cant be a solution.
There has to be exactly 1 of each digit and that means ther will be only 10 digits.

### <b>1. String Concatenation<b> ======================================
 -The following code would convert the ints into String.
 -Then we can concatenate them.
 -And then change it back into 1 large number.
 
int x = 12345;
int y = 678;
String str1 = String.valueOf(x);
String str2 = String.valueOf(y);
String str3 = str1.concat(str2);
System.out.println(str3);
int z = Integer.valueOf(str3);
System.out.println(z);

However it is an over kill involving the string class for something like this. 





### <b>2. String Concatenation with + operator<b> ======================================
 -The following code would be a quick fix for simple concatenations. BUT WITH CAUTION!
 -And then change it back into 1 large number.
 
int x = 12345;
int y = 678;
String str = "" + x + "" + y; 
System.out.println(str);
int z = Integer.valueOf(str);
System.out.println(z);

However, it internally uses a StringBuilder & it has cautions with null values.





### <b>3. With Pure Math Logic<b> ======================================
 -The following code would be perfect if you can change it to the real scenario! This is a hint
 -Numbers dont have concatenation... but there is a way you can make a new number that 
  looks like it has been joint by 2 other numbers.
 -CAUTION: the number you land up with could be too large for an int. Recall the limit of an int. 
  And you might need a larger data type than int.  
 
int x = 12345;
int y = 678;

x = 12345 * 1000;//increase the larger num
int z =  x + y; //10digits might not fit in int...!?
System.out.println(z);//this should look as if we have concatenated it

Adapt this code hint to the problem to successfully get a result that is still a number and looks
as if it has been concatenated without any string overheads!



 




</pre>
