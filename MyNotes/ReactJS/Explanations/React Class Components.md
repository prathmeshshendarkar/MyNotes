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