public class AddPair
 {
    public static int AddPair(int[] arr, int X) 
	{
        int count = 0; //Initialise count
		
        int begin = 0; // Initialise starting element of the array 
        int last = arr.length - 1; 

        while (begin < last) // Till the left element is less than the last element of the array follow the loop
		{
            int Sum = arr[begin] + arr[last]; //Initialise sum which is sum of first and the last element of the array

            if (Sum == X)
			{
               
                count++;
                begin++;
                last--;
            }
			else if (Sum < X) 
			{
               
                begin++;
            } 
			else 
			{
              
                last--;
            }
        }

        return count;
    }
	
	  public static void main(String[] args)
	  {
        int[] arr = {1, 2, 3, 4, 5}; //define array size and elements
        int X = 6; //define size of the sum
        int result = AddPair(arr, X); //calling the function defined above
        System.out("total relevant pairs "  is + result); //display result
    }
}








// Alternative logic that can be used in which everytime the left element is added to all the right elements and then the left element is incremented again untill we reach the penultimate element for the left element. Above logic is more efficient where left most and the right most elements are be ing incremented and decremented till all combinations are sumed up
