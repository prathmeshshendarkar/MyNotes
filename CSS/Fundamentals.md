### Modules in CSS
1. Since, any CSS File is global scoped, so every class that we declare in one css file, if there are multiple components with the same class names then for every component, that class properties will be applied
2. So, in order for us to have a local css scope only for particular component, we can create a local file and name it as `Anyname.module.css` 
3. After that, we can import the default object into our component using `import  Anyname from './Anyname.module.css'`
4. Now, inside the component, we can use these properties, like Anyname.classname

### Styled components in CSS
1. In order to use Styled components in CSS, we need to install the library first.
2. After that, inside any component, we can create a styled component like below code
```
const Nav = styled.component.nav`
	background-color: black;
`
```
3. This will create a new Nav component, that we can use in our render function like below
```
	render(){
		return <Nav />
	}
```

### Inline Styling
1. React also supports inline styling, which can be applied like below.
```
	<Nav className={{backgroundColor: 'blue'}}
```
2. The inline styling needs to have camel casing nature. So every property will have camel casing ability.

