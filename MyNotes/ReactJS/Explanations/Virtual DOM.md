## Virtual DOM
- In React, virtual dom is the exact replica of the original DOM of the page. 
- Whenever there is any changes in any node of the DOM, the children of that node will also get reloaded. However, react has introduced the concept of virtual dom which resides in memory.
- Whenever there is any changes in any node, the preDOM will get changed first, then it is compared with the virtual DOM which is called 'diffing'.
- Once JS get to know about these changes, the virtual dom will get changed called as 'Reconcilation'. And eventually only the node which needs to be changed in actual dom will be changed.