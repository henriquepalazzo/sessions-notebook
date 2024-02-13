# JS

ariables as elements used to describe a logic process. Allows you to plan or describe a logic without having the values themselves. 

Instead of using the class to select elements from the DOM, a better practice is to use the attribute data-js.

`const mainElement = document.queryselector('[data-js="main"]')`

## Arrays

const example = [1, 2, 'Bla', {}, undefined]

example[5] = 'new value'

**Add to the end**
example.push('new value not knowing the index')

**Retrieve from the end**
const lastValue = example.pop()

**Add to the beginning**
example.unshift('first value')

**Remove from the beginning**
const firstValue = example.shift()

**Important fact**
objects (including arrays) can't not be copied, the refer to the same element on memory

const arr1 = [1,2,3]
const arr2 = arr1

arr2.push(4)

console.log(arr1) // [1,2,3,4]

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

person['city'] = 'Berlim'

**Retrieving property with variable names**
Objects allow you to retrieve elements without specifying the key, or using a variable instead of the property key.

console.log(person[variable])

**Dot notation**
console.log(person.manager.name)