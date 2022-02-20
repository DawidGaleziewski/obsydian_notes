How much processes need to run to complete a task

## examples:

[[computational complexity]] $O(n)$. it would be 3n but we ignore coefficient.
```js
function crossAdd(input) {
  var answer = [];
	
	// for loops take longer the longer input is. Loops in general will affect greatly the processes that need to be performed. We should always check for loops. This is n^ of our equation
  for (var i = 0; i < input.length; i++) {
	// Things inside the loops are affecting our coefficient so 	 for example here 3n which we can ignore
    var goingUp = input[i];
    var goingDown = input[input.length - 1 - i];
    answer.push(goingUp + goingDown);
  }
  return answer;
}
```

Complexity $O(n)$. Despite the fact it will break once found a item, we always assume worst case scenario where the item we search is the last.
```js
function find(needle, haystack) {
  for (var i = 0; i < haystack.length; i++) {
    if (haystack[i] === needle) return true;
  }
}
```

Complexity $O(n^2)$. In general there are no $O(n^3)$ algorithms, those are going too far
```js
function makeTuplesFromArray(input) {
  var answer = [];

  // if we have 10 items it will iterate 10 times more for each item. Making it 100 iterations. The larger the input the more expenencial the growth. When we see nested loops by counting those we can know it will be n2, n3, n4 etc.
  for (var i = 0; i < input.length; i++) { // going n time
    for (var j = 0; j < input.length; j++) { // going n times once more
      answer.push([input[i], input[j]]);
    }
  }

  return answer;
}
```

Complexity $O(1)$ this is a perfect scenario as the ammount of operations will always be one
```js
function getMiddleOfArray(array) {
  return array[Math.floor(array.length / 2)];
}
```