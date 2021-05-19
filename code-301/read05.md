## React Docs - thinking in React

**How would you break a mock into a component heirarchy?**

By drawing boxes around every component (and subcomponent) in the mock and give them all names. 


**What is the single responsibility principle and how does it apply to components?**

> The Single Responsibility Principle represents a good way of identifying classes during the design phase of an application and it reminds you to think of all the ways a class can evolve. A good separation of responsibilities is done only when the full picture of how the application should work is well understand.

[Single Responsibility Principle](https://www.oodesign.com/single-responsibility-principle.html)


**What does it mean to build a ‘static’ version of your application?**

The easiest way is to build a version that takes your data model and renders the UI but has no interactivity. To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props.


**Once you have a static application, what do you need to add?**

You’ll want to build components that reuse other components and pass data using props. 


**What are the three questions you can ask to determine if something is state?**

- Is it passed in from a parent via props? If so, it probably isn’t state.

- Does it remain unchanged over time? If so, it probably isn’t state.

- Can you compute it based on any other state or props in your component? If so, it isn’t state.


**How can you identify where state needs to live?**

For each piece of state in your application:

- Identify every component that renders something based on that state.

- Find a common owner component (a single component above all the components that need the state in the hierarchy).

- Either the common owner or another component higher up in the hierarchy should own the state.

- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.




