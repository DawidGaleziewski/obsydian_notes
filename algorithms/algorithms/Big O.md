# Big O definition
Big O is the way to analyze how efficient [[algorithm]] is.
It is used to write down [[computational complexity]] or [[spatial complexity]] of a [[algorithm]]

* it tries measure how much time it takes given n inputs
* It avoid into goint into details. We measure the complexity by order of the magnitude. We do not care if function takes 300 milliseconds versus 330 milliseconds but if it takes 300 milliseconds vs 30 seconds. Example in formula: $3x^2 + x + 1$,  the [[term]] $3x^2$ carries the most weight. We take it and ignore coefficient. We are left with $O(n^2)$
* takes alway the worst case scenario. We do not care if algorithm could end after $1/2n$ we still assume the item we search for is at the last position

## examples

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

## common names for complexities

* $O(1)$ - constant
* $O(n)$ - linear
* $O(logn)$ - [[logarithmic]]
* $O(n^2)$ - quadratic

![[Pasted image 20220220193105.png]]