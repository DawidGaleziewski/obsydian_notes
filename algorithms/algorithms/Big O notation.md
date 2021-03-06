# Big O definition
Big O is the way to analyze how efficient [[algorithm]] is.
It is used to write down [[computational complexity]] or [[spatial complexity]] of a [[algorithm]]

* it tries measure how much time it takes given n inputs
* It avoid into goint into details. We measure the complexity by order of the magnitude. We do not care if function takes 300 milliseconds versus 330 milliseconds but if it takes 300 milliseconds vs 30 seconds. Example in formula: $3x^2 + x + 1$,  the [[term]] $3x^2$ carries the most weight. We take it and ignore coefficient. We are left with $O(n^2)$
* takes alway the worst case scenario. We do not care if algorithm could end after $1/2n$ we still assume the item we search for is at the last position


## common names for complexities

* $O(1)$ - constant
* $O(n)$ - linear
* $O(logn)$ - [[logarithmic]]
* $O(n^2)$ - quadratic

![[Pasted image 20220220193105.png]]