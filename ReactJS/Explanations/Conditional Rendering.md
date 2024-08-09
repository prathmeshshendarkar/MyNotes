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

