# Advanced
<h2>Improve Effeciency by almost 65%</h2>
<pre>
 - A pure observation will tell yout that numbers that end in 
0,1,5,6... will all have the same last digit in the 
square and in the cube! Hence they create a duplicate, and 
must be immediately ignored!

 - Another improvement can be observed by the final number
 having all the digits  0,1,2,3,4,5,6,7,8,9.
 This totals to 45... ie divisible by 3. 
 eg. if you rearrange them to form 5496287130 it is still
 divisible by 3. So another way to reduce checking,
 an entire number and its digits would be to....
 First check if its divisible by 3... then you could waste time
 creating an array from its digits!

### <b>Actual Advanced code<b> ======================================
 
 public class Exe69 {
    public static void main(String[] args) {

        
        for(int i=48; i<99; i++){
          //ignore the numbers that we know create duplicates
            int checker = i%10;
            if(checker==0 || checker==1 || checker==5 || checker==6){
                continue;
            }


            System.out.println("AT " + i);
            int sq = i*i;
            int cube = i*i*i;
            System.out.println(sq + " - " + cube);

            //int num = 9876543210;//this is an error due to int being too small
            long num = (cube * 10000L) + sq;
            System.out.println(num);

            if(num%3 != 0){//ignore if it cant be divisible by 3
                System.out.println("failed at Mod-3");
                continue;
            }


            int[] arr = new int[10];
            arr[0] = -1;

            for(int j=0; j<10; j++){
                int digit = (int) (num % 10);
                num = num/10;
                
                if(arr[digit]==digit){
                    System.out.println("DUPLICATE, broken at " + digit);
                    break;
                }
                else{
                    arr[digit] = digit;
                    System.out.println(Arrays.toString(arr));
                }

                if(j==9) {
                    System.out.println("================Looks like we have a winner..." + i);
                }
            }
        }

    }//xxxxxxxxxxxxxxxxxxx
}

 
 </pre>
