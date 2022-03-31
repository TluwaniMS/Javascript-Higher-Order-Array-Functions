# Javascript-Higher-Order-Array-Functions

`NB!` What are `Higher Order Functions`:

`Higher Order Functions` are functions that take in other functions as arguments or return functions.

`Javascript Higher Order Array Functions` call a `Callback Function` for each element in the array provided and return an array of values;
excluding `reduce()`.

1. `filter()`:

The `filter()` method returns new array with all the elements that satisfy the conditions required by the `Callback function` provided.

The `Callback Function` is invoked with three arguments:

* The value of the element

* The index of the element

* The array

`ArrayMethod(()=>{/*...*/})` or `ArrayMethod(function(){/*...*/})`

```
const numbersArray = [1, 2, 3, 4, 5];

const numbersDivisibleByTwo = numbersArray.filter((number) => !(number % 2));

console.log(numbersDivisibleByTwo);
///Will print:
[2,4]
```

2. `map()`:

The `map()` method returns a new array containing manipulated element properties or specific element properties that are set in the `Callback Function` provided.

The `Callback Function` is invoked with three arguments:

* The value of the element

* The index of the element

* The array

`ArrayMethod(()=>{/*...*/})` or `ArrayMethod(function(){/*...*/})`

```
const people = [
  { name: "Themba", gender: "male" },
  { name: " Thandi", gender: "female" },
  { name: "Lerato", gender: "female" }
];

const allNames = people.map((person) => person.name);

console.log(allNames);
///Will print:
[ 'Themba', ' Thandi', 'Lerato' ]
```

```
const numbersArray = [1, 2, 3, 4, 5];

const numbersMultipliedByTwo = numbersArray.map((number) => number * 2);

console.log(numbersMultipliedByTwo);
///Will print:
[ 2, 4, 6, 8, 10 ]
```

3. `forEach()`:

The `forEach()` method runs the logic provided in the `Callback Function` on each element in an array

The `Callback Function` is invoked with three arguments:

* The value of the element

* The index of the element

* The array

`ArrayMethod(()=>{/*...*/})` or `ArrayMethod(function(){/*...*/})`

```
const people = [{ name: "Themba" }, { name: " Thandi" }, { name: "Lerato" }];

people.forEach((person) => (person.email = `${person.name}@mock.com`));

console.log(people);
///Will print:
[
  { name: 'Themba', email: 'Themba@mock.com' },
  { name: ' Thandi', email: ' Thandi@mock.com' },
  { name: 'Lerato', email: 'Lerato@mock.com' }
]
```

4. `reduce()`:

The `reduce()` method runs a reducer `Callback Function` and returns a single value.

The `Callback Function` passed in the reduce method is invoked with four arguments:

* The previous value

* The current value

* The current index

* The array

`reduce((previousValue,currentValue,currentIndex,array)=>{/*...*/})` or `reduce(function(previousValue,currentValue,currentIndex,array){/*...*/})`

5. `sort()`:

The `sort()` method returns an array of sorted elements in ascending or descending order depending on the `Callback Function` passed in.

The `Callback Function` passed in the `sort()` method is invoked with two arguments:

* `a` the first element for comparison

* `b` the second element for comparison

`sort((a,b)=>{/*...*/})` or `sort(function(a,b){/*...*/})`

The `sort()` method by default sorts values as strings and sorts them in ascending order;

if ever an array of integers is passed the elements will be converted to strings and sorted according to eacch characters Unicode code point value.
