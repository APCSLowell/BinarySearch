Linear and Binary Searching Functions
==================

In this assignment you will write four searching functions:  
1. linearSearch  
2. recursiveLinearSearch   
3. binarySearch   
4. recursiveBinarySearch    

The functions are searching through an array of type `Item`. The `Item` class is defined as:
```Java
public class Item
{
    private int myCatNum, myInventory;
    public Item(int nNum, int nInv)
    {
        myCatNum = nNum;
        myInventory = nInv;
    }
    public int getCatNum(){return myCatNum;}
    public int getInventory(){return myInventory;}
}
```
Every `Item` has two integers, a catalog number and an inventory. Your functions will search for a catalog number. If the catalog number is found, the function will return the corresponding inventory. If an `Item` with that catalog number is not found, the function should return `-1`.   

Steps to complete the assignment
--------------------
1. First, complete the [codingbat searching problem set](https://codingbat.com/home/simona1@sfusd.edu/searching)
1. Fork and clone down this repository (Or fork [this repl.it](https://replit.com/@MrSimonLowell/BinarySearchBase#Sketch.java))
2. Write the four functions
3. Check your output. You should see the following:    
```   
Testing Linear Search   
Catalog #0 not found   
Catalog #183 not found   
Catalog #184 has 14 in stock   
Catalog #2370 has 65 in stock   
Catalog #15320 has 82 in stock   
Catalog #19967 has 45 in stock   
Catalog #19968 not found   

Testing Recursive Linear Search   
Catalog #0 not found   
Catalog #183 not found   
Catalog #184 has 14 in stock   
Catalog #2370 has 65 in stock   
Catalog #15320 has 82 in stock   
Catalog #19967 has 45 in stock   
Catalog #19968 not found   

Testing Non Recursive Binary Search   
Catalog #0 not found   
Catalog #183 not found   
Catalog #184 has 14 in stock   
Catalog #2370 has 65 in stock   
Catalog #15320 has 82 in stock   
Catalog #19967 has 45 in stock   
Catalog #19968 not found   
   
Testing Recursive Binary Search   
Catalog #0 not found   
Catalog #183 not found   
Catalog #184 has 14 in stock   
Catalog #2370 has 65 in stock   
Catalog #15320 has 82 in stock   
Catalog #19967 has 45 in stock   
Catalog #19968 not found   
``` 
//// C program to implement recursive Binary Search 
#include <stdio.h> 
  
// A recursive binary search function. It returns 
// location of x in given array arr[l..r] is present, 
// otherwise -1 
int binarySearch(int arr[], int l, int r, int x) 
{ 
    if (r >= l) { 
        int mid = l + (r - l) / 2; 
  
        // If the element is present at the middle 
        // itself 
        if (arr[mid] == x) 
            return mid; 
  
        // If element is smaller than mid, then 
        // it can only be present in left subarray 
        if (arr[mid] > x) 
            return binarySearch(arr, l, mid - 1, x); 
  
        // Else the element can only be present 
        // in right subarray 
        return binarySearch(arr, mid + 1, r, x); 
    } 
  
    // We reach here when element is not 
    // present in array 
    return -1; 
} 
  
int main(void) 
{ 
    int arr[] = { 2, 3, 4, 10, 40 }; 
    int n = sizeof(arr) / sizeof(arr[0]); 
    int x = 10; 
    int result = binarySearch(arr, 0, n - 1, x); 
    (result == -1) ? printf("Element is not present in array") 
                   : printf("Element is present at index %d", 
                            result); 
    return 0; 
} 
//

4. Submit the link to your GitHub or repl.it repository to google classroom

