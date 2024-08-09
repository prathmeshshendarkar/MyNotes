## UseRef
- This hook will give you a mutable object that can be referenced to any value , be it a number or any datatype or DOM Element as well.
- This hook can also be used as query selector when we want to select a DOM Element, in JavaScript we use `let xd = document.querySelector(asd)`.
- Similarly, after we declare a variable using this hook, we can assign it to a JSX Element using ref={yourRef} attribute.
- Properties of UseRef
	- This hook does not re-render the component.
	- It persists its value whenever the component is rendered.

- One of the best use case I encountered.
```
- When I wanted to use DOMELEMENT.scrollIntoView({smooth:scroll}); property
- Basically, whenever I click on any particular button, the view should smoothly scrolled to the selected DOM element.
- In that case, I can use the useRef to select that particular DOM Element and assign it to a JSX Element. Once a component renders with the toggle option I can either bring the DOM Element into my view or I can remove that element from the view.
```