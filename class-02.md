# Reading Notes - 301

## Mounting
When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase.

## Updating
Anytime a component is updated or state changes then it is rerendered. These lifecycle events happen during updating in this order.

## Unmounting
The final phase of the lifecycle if called when a component is being removed from the DOM.

## constructor()
The constructor for a React component is called before it is mounted.If the component is a subclass you should call super(props), or the props will be undefined. constructors can be used to assign state using this.state or to bind event handle methods to an instance.

## render()
Render is the only required method in a class component. It will examine this.props and this.state when called. The render function should not modify the component state because it would cause a lot of bugs by changing the state every time it rerenders. I also should not directly interact with the browser. render will not be invoked if shouldComponentUpdate() returns false.

![image](https://user-images.githubusercontent.com/83074494/125620155-985d9bc2-66d1-4b52-a31c-8283aae3018f.png)

