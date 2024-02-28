# JS

ariables as elements used to describe a logic process. Allows you to plan or describe a logic without having the values themselves. 

Instead of using the class to select elements from the DOM, a better practice is to use the attribute data-js.

`const mainElement = document.queryselector('[data-js="main"]')`

## Arrays

`const example = [1, 2, 'Bla', {}, undefined]`

`example[5] = 'new value'`

**Add to the end**
`example.push('new value not knowing the index')`

**Retrieve from the end**
`const lastValue = example.pop()`

**Add to the beginning**
`example.unshift('first value')`

**Remove from the beginning**
`const firstValue = example.shift()`

**Important fact**
objects (including arrays) can't not be copied, the refer to the same element on memory

`const arr1 = [1,2,3]`
`const arr2 = arr1`

`arr2.push(4)`

`console.log(arr1) // [1,2,3,4]`

## Objects

const person = {
	name: 'Tom',
	age: 34,
	isStudent: true,
	groups: ['admin', 'user'],
	manager: {
		name: 'Ana',
		age: 33,
		groups: ['admin']
	}
}

`person['city'] = 'Berlim'`

**Retrieving property with variable names**
Objects allow you to retrieve elements without specifying the key, or using a variable instead of the property key.

`console.log(person[variable])`

**Dot notation**
`console.log(person.manager.name)`

## Functions

**Function declaration**
function sum(a, b) {
	const result = a + b
	return result
}

**Function expression**
const sum = function(a, b) {
	const result = a + b
	return result
}

**IMPORTANT**
Function declaration allows you to call them anywhere in the code, even before the declaration, with function expression, that's not possible.

**Arrow function**
const sum = (a, b) => {
	const result = a + b
	return result
}

With only one parameter
const sum = a => {
	const result = a * a
	return result
}

With no parameter
const run = () => {
	logic
	return something
}

With only one statement (return)
const sum = (a, b) => a + b

With no parameter and only one statement
const run = () => something

## Strings



## Callback function

**Higher order functions**
A function that takes one or more functions as a parameter

**Referring x Calling**
Difference between referring to a function as a callback function (with no parenthesis) and calling it immediately (with parenthesis)

## Array methods

**Map**

Returning direct a value
`const whatever = array.map((element) => processedElement)`

Returning a code block
```
const whatever = whateverArray.map((element) => {
	some logic here
	return finalValue
})
```

**Difference between forEach and for**
The forEach will always complete all the cycles, there is no way of breaking it, even with a return statement inside the code block.

**Includes**
const arr [1,2,3,4]
arr.includes(2) // true

## Recurring functions

Powerful resource that should be used with care, specially regarding the need of having a defined stop command.

```
const arr = [1, 2, [3, 4], 5, [6, [7, 8]]]

function getElementCount(arr){
	let count = 0
	for (let i of arr) {
		if (Array.isArray(i)) {
			count += getElementCount(i)
		} else {
			count ++
		}
	}
	return count
}
```

## NPM

Package registry to control and have access to packages and other useful tools for the application. 

Dependencies x devDependencies
The second one should contain packages that are used or needed only for the development environment.

Versioning
The version number usually has a meaning and a reason on the way it's handled, usually the first number means a major change on the package, the ones that could potentially break the application, the second one are related to improvements and other changes that should not affect the functioning of the application, the last one is usually used for controlling bug and patches published to the package.

## Structure

Defer attribute forces the JS file to load only after the HTML is loaded. But it's not needed when we are working with modules attribute, that will automatically force the JS to be executed at the end.

## Special For Loops

Versatility of the for loop structure, being able to receive for instance an array as the first parameter, different types of incremente, even more than one comande as the iterator, separated by coma. One could use also with no parameters at all and using the code block to implement a logic that would break the loop when the condition is reached.

## Testing

Difference between static test and unit test. Static doesn't envolve code execution, basically is more related to syntax and will not find runtime errors. Unit test on the other hand verify that individual, isolated parts of the code works, given an specific input, test for the expected output. At the end, a group of unit test is called integration test.

End to end testing, also called e2e, consists in a robot that behaves like a user to click around the app and verify that it functions correctly.