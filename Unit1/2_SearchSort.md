# 1.2 Searching and Sorting Algorithms

## Searching Algorithms
Searching is a very common activity for computers to perform, so there are a few commonly-used algorithms out there to perform searching. An important thing to remember is that these are steps that the computer can perform one at a time--while humans can multitask at certain activities, computers, for our purposes, cannot.

### Linear Search
The simplest form of searching is a linear search. In a linear search, the computer goes through a list of items, one by one in a straight line and checks if there are correct. Once the computer has found the correct item, it is done.

1. If the current item is what we are searching for, we are done.
2. Go to the next item.

In the worst-case scenario (the item you are looking for is the last one), a linear search would have to check every single item in the list. That may be okay if it is only ten items, but it is slightly less okay if it is ten billion items, like what Google may have to search through when you type stuff into it.

### Binary Search
Binary search works differently than linear search by starting in the middle and using a "divide-and-conquer" type technique. Every time you check an item, either it is correct (in which case you are done), it is too high (in which case you can ignore everything beneath it), or it is too low (in which case you can ignore everything above it). Because it cuts the list in half every check, it is must faster than a linear search.

1. Look in the middle
2. If you find it, you're done!
3. If it's too high, throw out the bottom half
4. If it's too low, throw out the top half
5. Repeat

There is a catch to binary search, though, and it is a big one. Binary search only works if the list is in order. If the list is out of order, there's no way to predict what would happen if you tried to use this algorithm. You might get lucky and find the answer anyway, or, more likely, you would miss it, whether it was there or not.

Since binary search is so much faster than linear search, though, another common activity for computers to perform is to sort their data, or put it in order, so that it will be ready to be quickly searched through when the time comes.

## Sorting Algorithms
When humans sort things, we often like to make two separate sets, one for the sorted items, and one for the ones we have not sorted yet. Computers often deal with lists so long that they do not have the luxury of enough space to keep two whole lists, so they often use sorting algorithms that sort the lists where they are, by swapping individual items around. Because of this, they are often a little more difficult to comprehend than the searching algorithms above.

### Selection Sort [¹](#footnote1)
1. Find the smallest item. Swap it with the first item.
2. Find the second-smallest item. Swap it with the second item.
3. Find the third-smallest item. Swap it with the third item.
4. Repeat finding the next-smallest item, and swapping it into the correct position until the list is sorted.

These steps for the selection sort how complex this algorithm actually is. Step 1 starts with “Find the smallest item.” How do we do that? That step by itself requires its own algorithm. Many algorithms are built on top of other algorithms. Solving large problems often involves breaking them down into smaller, easier-to-solve parts and reassembling them at the end. Finding the smallest number can be done with an algorithm similar to linear search.

### Bubble Sort
1. Check the first two items
2. If the second item is less than the first item, swap them
3. Repeat steps 1 and 2 for the second/third items, the third/fourth items, until you reach the end of the unsorted list
4. The last item of the unsorted list is now sorted
5. Repeat steps 1 to 4 until there are no more unsorted items

In a bubble sort, the items gradually "bubble" their way toward the right end of the list, with one item reaching the right spot in each cycle.

### Insertion Sort
1. The first item will be considered part of the sorted list
2. For each item in the unsorted list, back it up into the sorted list as long as it is greater than the item before it.

Insertion sort works a little like the way people work. One item is picked each cycle, its place in the sorted part of the list is found, and it is placed there.

## Questions
(Tip: You can practice sorting using [this interactive page](http://www.gilfusion.com/ListItemSwap.html) that lets you keep split the list in parts and swap numbers.)

1.  Which search algorithm would you use to find an item in the following list and why?
    * Alex
    * Bonnie
    * Colin
    * Danielle
    * Earl
    * Fiona
2. Which search algorithm would you use to find an item in the following list and why?
	* Hermione
    * Richard
    * Nicole
    * Gaston
    * Paula
    * Igor		
3. Write the following numbers down in pencil on a piece of paper: 12, 76, 47, 32, 99, 11, and 63. Try following the directions for a bubble sort to put the numbers in order, erasing and rewriting the numbers for each swap.
4. Write the following numbers down in pencil on a piece of paper: 36, 99, 21, 74, 11, and 67. Try following the directions for an insertion sort to put the numbers in order.
		
## Notes
¹ <a id="footnote1"></a>Source: https://www.khanacademy.org/computing/computer-science/algorithms/sorting-algorithms/a/selection-sort-pseudocode