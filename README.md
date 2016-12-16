#Array Cardio Day 2

## [`some()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
`some()` takes a predicate function and returns `true` if at least some of the items in the collection pass truth test

```js
const people = [
  { name: 'Wes', year: 1988 },
  { name: 'Kait', year: 1986 },
  { name: 'Irv', year: 1970 },
  { name: 'Lux', year: 2015 }
];
// Are some of the people at least 19 years old?

  const isAdult = people.some(person => 
    new Date().getFullYear() - person.year >= 19);

  console.log({isAdult})
  // >> isAdult: true
```

##`every()`
`every` returns true if all items in the collection pass a truth test
```js
// Is everyone in the list at least 19?

  const allAdults = people.every(person =>
    new Date().getFullYear() - person.year >= 19);

  console.log({allAdults})
// >> allAdults: false
```

##`find()`
`find` is like filter, it returns only one item. The first item in the collection that passes a truth test.

```js
// Find the comment with an id of 823423

  const comment = comments.find( comment => comment.id === 823423);
  console.log({comment})

// {id: 823423, text: "Super Good"}
```


##`findIndex()`
`findIndex` returns the index number of the first item passing a truth test

```js
// Find where in the array comment id 823423 is so we can delete it
  const index = comments.findIndex(comment => comment.id === 823423);
  console.log( index )
// it's index is 1

// We can use `slice()` to remove the item at that position
const newComments = [
	// without the spread operator, this returns a nested array
  ...comments.slice(0, index), // from 0 to the index
  ...comments.slice(index+1)  // from the positin after the index onward
  	// spread both slices to return an flat array
];
```










