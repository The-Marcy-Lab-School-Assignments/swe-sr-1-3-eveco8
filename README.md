# swe-sr-1-3

## Setup

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/how-tos/working-with-assignments#how-to-work-on-assignments).

Here are some useful commands to remember.

```sh
npm i                   # install dependencies
git checkout -b draft   # switch to the draft branch before starting

git add -A              # add a changed file to the staging area
git commit -m 'message' # create a commit with the changes
git push                # push the new commit to the remote repo
```

## Question 1

Read the documentation for `findIndex` and `indexOf` on MDN:

- [findIndex](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
- [indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf).

Explain the difference between the methods and explain when you would choose one over the other. Provide examples to enhance your response.

### Response

#### What is `findIndex`?

- Iterates through a given **_array_** and searches for **_element_** using a **_callback function(condition)_**
- Can search through **_objects in arrays_**
- Returns the index of the first element that passes the condition

##### Syntax

```JavaScript
array.findIndex(callbackFunction)
```

##### Example

```JavaScript
    const users = [
        { id: 1, name: 'Evelin'},
        { id: 2, name: 'Katrina'}
    ];

    console.log(users.findIndex(user => user.name === 'Katrina')) // 1
```

In the example above, we use `findIndex` to find the **_index_** of the first name that passes the condition. In this case, the first name is Katrina and the index of it is 1. If there were more objects with this name the the output would still be 1 since it is the first to pass the condition. If nothing passes the condition then the output will be -1.

#### What is `indexOf`?

- Iterates through an **_array_** and searches for the **_index_** of the value you give it
- Will start search in array at any index you provide but will _default to index 0_
- Works best to find _strings or numbers_ in an array
- _Cannot work_ in _objects_
- Returns the index of the element or -1 if nothing is found

##### Syntax

```JavaScript
array.indexOf(searchElement, fromIndex)
```

##### Example

```JavaScript
const nums = [2, 4, 3, 6, 9]

nums.indexOf(3) // 2
```

In the example above, we use `indexOf` to find the index of number 3 in the array. In this case, number 3 is at index 2.

#### Their differences

Both are methods on an array that can be used to find the index of elements. However, `indexOf` searches for a specific element while `findIndex` uses a condition to search for an element.

#### When to use

- Use `indexOf` when searching for _a specific value_ like a string or number.

- Use `findIndex` when searching _though objects_ or when you need to _use a condition_ if you're not searching for an exact value.
