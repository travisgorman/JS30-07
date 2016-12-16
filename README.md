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
