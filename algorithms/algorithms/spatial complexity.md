How much space (RAM or disk space) a algorithm needs to complete

## examples:

```js
const createArray = (n) => {
	const answer = [];
	
	n.forEach(item => {
		answer.push(item)
	})
}
```

## trivia

Most times spatial complexity wont matter. But when it does it makes a huge impact. Example of this could be systems that do not have much memory.

functional programming tends to be more expensive on the spatial aspect as there are many arrays created and destroyed.