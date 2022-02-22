# Bubble sort

[[computational complexity]] $O(n^2)$ - every item in array needs to make contact with every other item
[[spatial complexity]] $O(1)$ - we are not creating any other arrays it just stays as one array that was provided in memory

Best case scenario $O(n)$ for sorted list
Worst case scenario $O(n^2)$ for reverse sorted list

It is a [[stable sort]] and a [[destructive sort]]

![[Pasted image 20220221202034.png]]

Compare two items in an array that are next to each other, if they are out of order swap them.

![[Untitled.jpg]]

It is a algorithm that matches human mental model.
Not a algorithm that would be used in a production

## Optimitisations

Due to the fact that after first iteration, the largest number will "bubble" to the end of array we know there will be no need for swapping end of the array. The more swaps we do the sorter part of the array we have to check.

```js
// Array
[5,2,1,5]

//First loop the 5 was pushed to the top
[2,1,5,5]

```

