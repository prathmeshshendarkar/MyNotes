# React

## Features of react
1. Declarative
2. Component based
3. Efficient for creating SPA's because of virtual DOM's

## CDN Links
1. React
        <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
		<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
2. Babel	
	<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
	
## React is ...
1. Library to build user interfaces.
2. Composable(Components based) so, Reusable components.


## How to add react elements to our ReactDOM
1. Creating a element
	- const img = React.createElement('img', {src:$url}};
2. Adding/Rendering the element to our React DOM Tree
	- ReactDOM.render(img, document.getElementById('root'));
	
The above two steps will first create a react element and the second step will render the element onto our react dom tree.

## Virtual DOM
- In React, virtual dom is the exact replica of the original DOM of the page. 
- Whenever there is any changes in any node of the DOM, the children of that node will also get reloaded. However, react has introduced the concept of virtual dom which resides in memory.
- Whenever there is any changes in any node, the preDOM will get changed first, then it is compared with the virtual DOM which is called 'diffing'.
- Once JS get to know about these changes, the virtual dom will get changed called as 'Reconcilation'. And eventually only the node which needs to be changed in actual dom will be changed.


## Babel in React.
- Babel is the transpiler for newer syntax of JS. These newer syntax of JS like JSX is not supported by old browser. Babel will compile the JSX into plain JS code which older browser supports.

## Fragments in React
- JSX Cannot allow multiple elements attached to a single variable, so in this case we need to use react fragments and inside those fragments we can have multiple elements.


## Components in React
- First we need to understand that, react only allows the components that start with the capital letter. So naming convention should be cleared.
- Next, when we call the component, we are not allowed to call it like a function(App()), We need to call these components as <App /> then only it will be considered as component based.

## JSX in React
- To use a variable inside react component use {}
- 

## React Class Components
1. Class ComponentName extends React.Component {
	constructor(){
		super();
		this.state = {}
	}
	render (
		<div></div>
	)
}

2. Whenever you are using constructor in a class based component, and since you must have inherited react component, by default you will need to call the inherited constructor as well, which is possible by writing super keyword.
3. `super()` will simply execute the parent class’s constructor. If you are inheriting from other classes and you use the constructor in your child class, then you have to call `super()` inside the constructor of your child class otherwise it will throw an error.

## Binding this keyword in a class
1. In a event handler when we do like this onClick = {this.addNums} and if we try to console.log this.state inside of that addNums function, it won't work. We need to find this to addNum, onClick = {this.addNums.bind(this)} in order for this to work
2. Next is we can also add the above bind function directly inside the constructor that also works.
3. If we do not want to bind and all, just create a constructor function of addNums and that automatically binds this to addNums.

## Setting State
1. After creating a state object inside the constructor and if we want to alter any particular thing inside the state, we can use this.setState = {}
2. We can use this.setState two ways
	a. this.setState({nums: nums+1});
	b. this.setState((prev) => {prev.nums += 1}) ----- This takes a callback function inside setState
3. setState is asynchronous in nature, so while setting the setting a state of any parameter, if we want to find the value of that parameter react allows us to use callback functions in setState.
	this.setState({nums: nums+1}, () => {console.log(nums)});
4. If we have multiple calls for setState inside a function, then only one setState will be executed. For ex: 
```
	1. handleClick() {
    // console.log("I am clicking");
    const moodIndex = Math.floor(Math.random() * MOODS.length);
    this.setState({ prediction: MOODS[moodIndex] });
    this.setState({ nums: this.state.nums+1 });
    this.setState({ nums: this.state.nums+1 });
    this.setState({ nums: this.state.nums+1 });
    this.setState({ nums: this.state.nums+1 });
    console.log(this.state.nums);
  }
```


## Conditional Rendering
1. When we want to toggle certain things, for ex: A state of button needs to be changed as we click to true or false.
2. Conditional rendering allows us to render different components or elements based on certain conditions.
3. There are three types of rendering 
	1. If else statement
	2. Ternary Operator: {`this.state.fav?<Home/>:<Login/>`}
	3. Logical And Operator `{isLoggedIn && <Home/>}`
4. *Now, Conditional rendering not only allows us to render components or elements, we can also use this methods to toggle classNames inside of components.*
	1. For Ex: `<button className={this.state.fav?"toggleOn":toggleOff} />`


Props
1. Props or attributes of any components can only be passed from parent to child. They cannot be passed in between siblings.
2. If we sometimes forget to pass the props from parent to child then we can have a defaultProps object in the Parent component. The child component will take that value from defaultProps object from parent component to insert the value.
3. Props cannot be changed in the child component.

### CSS

Number of ways to style in reactjs components.
#### Modules in CSS
1. [[CSS/Fundamentals|Fundamentals]]
#### Styled Components in CSS
1. [[CSS/Fundamentals|Fundamentals]]
#### Inline Styling
1. [[CSS/Fundamentals|Fundamentals]]

