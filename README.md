# SubArray

Given an array arr[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10} of size 10. Find whether there exists a sub-array of size n and sum s, where n and s both are user input values.

Print YES if there exists a subarray of size n and sum s in the array arr else print NO

Input Format
The first and only line of input contains n and s

Output Format
Print either “YES” or “NO”

Example 1
Input

3 6
Output

YES
Explanation

The sum of elements at indices 0, 1,2 add upto 6

Example 2
Input

4 10
Output

YES
Explanation

The sum of elements at indices 0, 1, 2, 3 add upto 10

Constraints
1<=n<=10 1<=s<=55


///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


import java.util.*;

public class Main
{

  public static void solve (int[]arr, int n, int s)
  {
    //first we going to index n;

    boolean found = false;
    for (int i = 0; i < arr.length - n + 1; i++)
      {
	int currentSum = 0;
	for (int j = i; j < i + n; j++)
	  {
	    currentSum += arr[j];
	  }
	if (currentSum == s)
	  {
	    found = true;
	    break;
	  }
      }
    if (found)
      {
	System.out.println ("Yes");
      }
    else
      {
	System.out.println ("NO");
      }

  }

    public static void main (String[]args) throws Throwable
  {
    Scanner sc = new Scanner (System.in);
    int[] arr = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
    int n;
    n = sc.nextInt ();
    int s;
    s = sc.nextInt ();
    solve (arr, n, s);
  }
}
