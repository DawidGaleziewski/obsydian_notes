Insertion sort divides array into two arrays sorted and unsorted.
It starts with just one item so for example:

```js
const nums = [5,2,5,7,8]

const sortedArray = [5];
const unsortedArray = [2,5,7,8];
```

[[computational complexity]] is $O(n^2)$
[[spatial complexity]] is $O(1)$
It is still a decent sort for lists that are shuffled and mostly sorted. 
Fpr example we have logs from a server with UDP request that are mostly in order but sometimes get out of line. This is a perfect use case

It is a [[stable sort]] and a [[destructive sort]]

We can immagine we have a marker that we are going from left to the right. We are comparing with number to the right. If it is larger

## code example

```js

function insertionSort(nums) {
  let sortedIndex = 0;

  for (let i = 0 ; i < nums.length){
    if (nums[i] > nums[sortedIndex]){
      
    }
  }
}

const arr = [2,3,5,1,3];

console.log(insertionSort(arr))
```