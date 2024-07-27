## Components Lifecycle Phases & Methods
1. There are 4 phases for any component build using react: Mounting, Updating, UnMounting and Error Handling.
2. Each phase has a different lifecycle method associated to it. So in what order should these lifecycle method should be executed is important.
### Mounting Phase
1. There are 4 lifecyle methods in Mounting Phase: constructor, getDerivedStatefromProps, render, componentDidMount
2. Constructor: 
	1. Constructor are used to initialize the state or bind the event handlers to the component instance(this.eventHandlerFunction.bind(this))
	2. Side Effects: Avoid any side effects inside of constructor.
	3. Avoid setting the state inside the constructor function.
3. getDerivedStateFromProps:
	1. This method is called just before the render function. Even when the component is re-rendered, this method is always called before the render function.
	2. Same as other methods, avoid side effects in this method as well.
4. Render:
	1. Render method is the required method in react, which returns us the JSX.
	2. Avoid Side effects in render method and also avoid setting state in Render method.
	3. Render functions should be Pure functions. Pure functions are those which provides output to whatever input we provide.
5. componentDidMount:
	1. This method is called after the component and it's childrens are mounted on the DOM.
	2. Side Effects: Allowed to perform side effects like calling any API.
	3. Setting State; Allowed to set state in this method.
6. After we set the state in componentDidMount, the component is called again and then first getDerivedStateFromProps is first called then Render method is called.

### Side Effects in ReactJS
1. Side Effects are those calls and actions that are performed outside of react. For ex: When we fetch the data using http request, When we call the browser API(Since react does not support that), Manipulating DOM using Native DOM Syntax.

### Updating Phase
1. There are 6 lifecycle methods involved during this phase. Whenever the state is changed, component is re-rendered. Before this re-rendering there are few methods and after that there are few methods.
2. getDerivedStateFromProps()
3. shouldComponentUpdate() : This method is called before render function and returns a boolean value, if the component should be updated or not? By Default it returns true.
4. render()
5. getSnapShotBeforeUpdate() : This method returns a snapshot of the component just before virtual dom changes it's node from current state to real dom.
6. componentDidUpdate() : This method is where we can set the state again and use side effects.
7. Remember only componentDidUpdate is allowed for setting state and side effects. Whereas in all other methods, it is not recommended.

### Unmounting Phase
1. There is only one method in this phase, componentWillUnmount() : This method will 
