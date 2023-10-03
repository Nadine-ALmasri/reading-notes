## Conditional rendering 
Conditional rendering in React allows you to selectively display components based on application state, similar to JavaScript conditions. You can use if statements or the conditional operator for this.

Example: A Greeting component renders either a "Welcome back!" or "Please sign up." message depending on the isLoggedIn prop.

You can use variables to store elements for conditional rendering, providing flexibility in JSX. Example: LoginControl renders either a login or logout button based on state.

React supports inline conditions in JSX using the logical && operator and the conditional operator condition ? true : false. This allows for concise and readable conditional rendering within components.

## Links and Key:
In React, rendering lists of elements is similar to JavaScript's map() function. You can create collections of elements and include them in JSX using curly braces {}. For example, you can loop through an array and create a list of elements like <li> within a <ul> element.

Keys are essential in React when rendering lists to help React identify changes, additions, or removals of list items. Keys should be unique among siblings. They can be based on unique IDs from your data or, as a last resort, the index of the item in the list. Avoid using indexes as keys if the order of items may change.

When extracting components from a list, ensure that the key is specified on the outermost component within the map() function, not on individual elements inside the extracted component.
## Controlled Components:

In controlled components, React manages the form element's state, making it the "single source of truth" for the input value.
This means that the value displayed in the form element is always driven by the React state, which is updated using the setState() method.
Controlled components are useful for handling form submissions and maintaining input data integrity.
## inheritance
React promotes composition over inheritance for building reusable components. Here are the key points regarding composition vs. inheritance in React:


## Containment:
Components that don't know their children ahead of time can use the children prop to pass arbitrary children elements.
This allows other components to nest JSX elements within a component, and those elements become the children prop of the component.

## Specialization:
Components can be thought of as special cases of other components.
Specialization is achieved through composition, where a specific component renders a more general one and configures it with props.

## Composition for Reuse:

In React, you can achieve code reuse through props and composition rather than creating complex inheritance hierarchies.
Props and composition provide the flexibility needed to customize a component's appearance and behavior explicitly.
## Avoiding Inheritance:

React recommends avoiding the creation of component inheritance hierarchies.
Instead, reuse non-UI functionality by extracting it into separate JavaScript modules that can be imported and used by components.

In summary, React's composition model, using props and the children prop, provides a more flexible and safer approach to building reusable components compared to traditional inheritance. By following this approach, you can create more maintainable and extensible component architectures.
 
 
 
 
 
 
 
 
 
 
 
 
 
 ## Thinking in React

 When working with React, it's essential to adopt a different mindset for designing user interfaces and applications. This tutorial guides you through the thought process of building a searchable product data table with React, helping you understand React's approach to building UIs.
 ## Start with the Mockup:

Description: Begin your React project by imagining you already have a JSON API and a mockup from a designer. The JSON API provides data that represents the products you want to display.
## Break the UI into a Component Hierarchy


The first step in building a React app is to break the user interface into a component hierarchy. This process involves identifying different components in your mockup and organizing them hierarchically. Learn how to name and structure your components based on their responsibilities and relationships.
## Build a Static Version in React

Once you have your component hierarchy, you'll start building a static version of your app. In this phase, you focus on rendering the UI using React components without adding interactivity. By doing so, you create reusable components and establish the foundation for your dynamic app.

Find the Minimal but Complete Representation of UI State

Description:
To make your app interactive, you need to identify the minimal set of stateful data required. Learn how to determine which parts of your app's data should be considered state and which should be passed as props. This step helps you keep your application organized and efficient.

## Identify Where Your State Should Live


After defining your app's state, you need to decide where this state should be managed. Understand the principles of managing state in React, including identifying components that need access to the state and determining the appropriate location for state management.

## Add Inverse Data Flow


In this final step, you'll enable user interaction by adding inverse data flow. Learn how to pass data from child components to parent components, allowing user actions to update the app's state. By setting up this two-way communication, your React app becomes fully interactive.