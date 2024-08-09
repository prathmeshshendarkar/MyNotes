## How to add react elements to our ReactDOM
1. Creating a element
	- const img = React.createElement('img', {src:$url}};
2. Adding/Rendering the element to our React DOM Tree
	- ReactDOM.render(img, document.getElementById('root'));
	
The above two steps will first create a react element and the second step will render the element onto our react dom tree.