# Reading Notes - 301

Sources
- Assigned reading from https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm
- Assigned reading from https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0

#Component-Based Architecture

## What is a component?
A component is a small piece of code that fills a certain part of the UI that you're building with React. A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

### Characteristics of Components:
Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.

Replaceable − Components may be freely substituted with other similar components.

Not context specific − Components are designed to operate in different environments and contexts.

Extensible − A component can be extended from existing components to provide new behavior.

Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.

Independent − Components are designed to have minimal dependencies on other components.

### Advantages
Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.

Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.

Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.

Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

# What is Props and how to use it in React

## What is a Props short for?
“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.
But the important part here is that data with props are being passed in a uni-directional flow. (one way from parent to child)
Furthermore, props data is read-only, which means that data coming from the parent should not be changed by child components.

## How are Props used in React?
- Firstly, define an attribute and its value(data)
```
<ChildComponent someAttribute={value} anotherAttribute={value}/>
<ChildComponent text={“I’m the 1st child”} />
```
- Then pass it to child component(s) by using Props
passed through a function:
```
const addition = (firstNum, secondNum) => {  
  return firstNum + secondNum; 
};
```
passed through a React component:
```
const ChildComponent = (props) => {  
  return <p>I'm the 1st child!</p>; 
};
```
- Finally, render the Props Data
```
const ChildComponent = (props) => {  
  return <p>{props.text}</p>; 
};
```
```
class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent text={"I'm the 1st child"} />
        <ChildComponent text={"I'm the 2nd child"} />
        <ChildComponent text={"I'm the 3rd child"} />
      </h1>
    );
  }
}
```
## What is the flow of Props?
The flow is One-Way and down, passed from the parent component to the child component.
