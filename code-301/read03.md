## React Docs - lists and keys

**What does .map() return?**

A Map object iterates its elements in insertion order, a for...of and afor...in loop returns an array of [key, value] for each iteration.

**If I want to loop through an array and display each value in JSX, how do I do that in React?**
We loop through the array using the JavaScript map() function. 

For example:

const numbers = [1, 2, 3, 4, 5];

const listItems = numbers.map((number) =>{

  return numbers

});

**Each list item needs a unique:** li element (unordered list tag < li> </ li>).

**What is the purpose of a key?**

A “key” is a special string attribute you need to include when creating lists of elements. Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.


## The Spread Operator

**What is the spread operator?**

 The spread operator is a syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

**List 4 things that the spread operator can do.**

- Copying an array.
- Concatenating or combining arrays.
- Using Math functions.
- Using an array as arguments.
- Adding an item to a list.
- Adding to state in React.
- Combining objects.
- Converting NodeList to an array.

**Give an example of using the spread operator to add a new item to an array.**

* Example 1:

const number1=[ 1,2,3]

const number2=[10,20, ...number1]

* Example 2:

const finalName=[ 'Baba']

const fullName=['Layana','Ayman', ...finalName]

**Give an example of using the spread operator to combine two objects into one.**

* Example 1:

const objectOne = {hello: "Welcome,"}

const objectTwo = {name: " Israa"}

const objectThree = {...objectOne, ...objectTwo}

* Example 2:

const objectOne = {question: "How do you feel about reading assignment?"}

const objectTwo = {name: " hate it very much."}

const objectThree = {...objectOne, ...objectTwo}


## How to Pass Functions Between Components

**In the video, what is the first step that the developer does to pass functions between components?**

Creating an increament function.

**In your own words, what does the increment function do?**

Increament function can update the count inside peaple, when the user click on add button.

**How can you pass a method from a parent component into a child component?**

- Define your parent callback function in your parent component.
- Pass the function to the child component.
- Set up an input variable in child component.
- Call the callback function.

**How does the child component invoke a method that was passed to it from a parent component?**

- Create a child component and put the below code inside that component.
- import the child component to parent component.
- Then inside parent function create another function to run desired event and pass the child component to return.