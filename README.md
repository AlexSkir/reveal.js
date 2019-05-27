# Transcript of presentation

#### slide 2

React is a JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”. Some people call it a framework, but actually it's not. React is just a view layer. So it is not directly comparable to frameworks like angular.

#### slide 3
Popularity of React is growing. And there are just some features why more and more professionals chose this library for their projects: 
- first of all it's fast, you can maintain updates of your applications without loss of performance. 
- other benefit is modularity of React, which helps to keep the code cleen and easier to support. 
- Scalability is another appealing feature, that allows to extend functionality without large changes in code. 
- Also, React can be used to create very different types of projects, people are still figuring out React’s potential.

#### slide 4.1
Few words about statistics. 
This line chart represents the dynamics of the popularity of web search by key words React Angular and Vue since 2013-th to the present day in Russia 
As we can see the level of interest to React increased significantly during that time, outgrowing Angular and reaching the peak in last year. And this trend remains stable.

#### slide 4.2
Quite similar situation in trends worldwide with slight differences.

#### slide 4.3
there is a regional representation of interest to React Angular and Vue across the world.

#### slide 5
Notable features of React: JSX, props, state, virtual DOM, lifecycle methods.

#### slide 6.1
JSX or JavaScript XML is an extension to the JavaScript language syntax. It combines JS and HTML syntax. HTML part may contain some text enclosed in tags such as 'headings', 'paragraphs' and others. 
And we can add attributes like in common HTML, such as source in 'image' tag in the example.

#### slide 6.2
JavaScript expressions also can be used inside JSX blocks if they are enclosed in curly braces. 
JSX provides a way to structure component rendering.

#### slide 7.1
Every component has properties or shortly - props. A component’s props is an object. It holds information about that component. 
We can pass props to a component by adding attribute with name and value, as shown on the 8th line in the example 
We used that props in H1 heading tag on third line, so it's value will be displayed on the web page.

#### slide 7.2
Props can also be used to make decisions, as shown in this example. Class Greeting accepts two Props 'name' and 'signed in'. The information displayed on the web page will depend on the value of 'signed in' prop.

#### slide 7.3
A component can pass information to another component. 
In order to do that you should export the component from the first js file using key word "export".

#### slide 7.4
and import that component to the second js file which we did on line 3. Then, we used the instance of greeting in App component (line 10), so h1 heading from greeting component will be rendered on the web page below "Hello and welcome!".

#### slide 8.1
A React component can access dynamic information in two ways: props and state. Unlike props, a component’s state is not passed in from the outside. A component decides its own state. 
To set a state property you should declare it inside of a constructor method, calling parent constructor with key word 'super'. 
this.state should be equal to an object, like in the 4th line. 
As props, state also can be read and displayed on web page using the expression this.state.name-of-property in curly braces.

#### slide 8.2
The state can be changed by calling the function this.setState() like in line 9. 
The most common way to do that is to call a custom function like toggleMood in the example. It wraps a this.setState call. 
When button is clicked the state changes and it AUTOMATICALLY calls render method so we can see changes immediately.

#### slide 9
Another notable feature is the use of a "virtual Document Object Model". React creates an in-memory data-structure cache, computes the resulting differences, and then updates the browser's displayed DOM efficiently. 
This allows the programmer to write code as if the entire page is rendered on each change, while the React libraries only render subcomponents that actually change.

#### slide 10.1
Lifecycle methods are methods that get called at certain moments in a component’s life. 
There are three categories of lifecycle methods: mounting, updating, and unmounting.

#### slide 10.2
A component “mounts” when it renders for the first time. There are three mounting lifecycle methods: 
componentWillMount, render and componentDidMount. 
"componentWillMount" gets called right before render, then component renders, and componentDidMount gets called right after the HTML has finished loading.

#### slide 10.3
A component updates every time that it renders, starting with the second render and it automatically calls all five of its methods, in order. 
- "componentWillReceiveProps" gets called before the rendering begins and only gets called if the component will receive props. 
- "shouldComponentUpdate" should return either true or false. If shouldComponentUpdate returns true, then component updates if returns false, then the component will not update! None of the remaining lifecycle methods for that updating period will be called, including render. 
- The main purpose of "componentWillUpdate" is to interact with things outside of the React architecture before a component renders, for example to check the window size or to interact with an API. 
- When a component instance updates, "componentDidUpdate" gets called after any rendered HTML has finished loading. "componentDidUpdate" is usually used for interacting with things outside of the React environment, like the browser or APIs. It’s similar to componentWillUpdate in that way, except that it gets called after render instead of before.

#### slide 10.4
A component’s unmounting period occurs when the component is removed from the DOM. This could happen if the DOM is rerendered without the component, or if the user navigates to a different website or closes their web browser. 
"componentWillUnmount" is the only unmounting lifecycle method. It gets called right before a component is removed from the DOM. If a component initiates any methods that require cleanup, then "componentWillUnmount" is where that cleanup should be put.

#### slide 11.1
In react data flows in one direction from parent to child. With this characteristic, it's not obvious how two non parent-child components would communicate. Direct component-to-component communication is error prone and leads to spaghetti code. This is where Redux can help.

#### slide 11.2
Redux is a small library with a simple, limited API, designed to be a predictable container for application state. Redux offers a solution of storing all your application state in one place, called a "store". Components then "dispatch" state changes to the store, not directly to other components. The components that need to be aware of state changes can "subscribe" to the store.

#### slide 11.3
Redux uses only one store for all its application state. Since all state resides in one place, Redux calls this the single source of truth. The data structure of the store is typically a deeply nested object. 
Such an approach reduces errors and makes it much easier to pass and access the props and state.
