# Step 2
<h2>Number Concatenation</h2>
<pre>
After getting the number we are on(atm in the for loop via <b>i</b>) we have saved its square and cube to 2 separate int variables.

Now we need to join them.. ie concatenate them. And in doing so we will observe all the digits 0123456789. 
Please note there can be no repeat of a digit... if there is a digit that repeats for eg 012344456789 .. it cant be a solution.
There has to be exactly 1 of each digit and that means ther will be only 10 digits.

<b>String Concatenation<b>
 -The following code would convert the ints into String.
 -Then we can concatenate them.
 
        int x = 12345;
        int y = 678;
        
        String str1 = String.valueOf(x);
        String str2 = String.valueOf(y);
        String str3 = str1.concat(str2);
        
        System.out.println(str3); 
However it is an over kill involving the string class for something like this.        
 




</pre>
