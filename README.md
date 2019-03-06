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
1. Fork and clone down this repository
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

4. Submit the link to your GitHub repository to google classroom

