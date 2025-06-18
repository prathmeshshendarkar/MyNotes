1. Constructor functions are created only using normal functions and we cannot create a constructor function using arrow functions
2. Constructor function are instantiated into an object using new keyword. Below is the code for a sample constructor function
3. ![[Pasted image 20240714232717.png]]
4. Now, if you see , we have also passed one argument while calling the constructor function. The name parameter is only accessible within the local context of that constructor function.
5. That parameter is not linked to the instantiated object(aliceFunc). In order to link the name parameter to the instantiated object, we need to use ***this*** keyword. For ex:
6. ![[Pasted image 20240714233442.png]]


## Constructor function inside of class
1. Below is the code to create a constructor function inside a class. There are few things to remember when we create methods inside the class.
2. ![[Pasted image 20240715001118.png]]
3. In the above code, what is our process?
	1. We first created a class with a constructor function that will bind the name parameter to the instantiated object(aliceClass)
	2. Then we created a method (adds) which will return the addition of two numbers.
	3. Next we created a instance of that class.
	4. Then, we called the method adds from the instantiated object. 
	5. And lastly, we called the same method from the class's prototype object.
4. Now, if you must have understood that, a normal function won't bind to the instantiated object. It will go to the prototype of App class.
5. The reason for aliceClass.adds(1,2) is working because of ***prototype chaining*** in javascript. Where, if the object is not able to find the method, it will look into the parent's prototype object.
6. Whereas, if we create a Arrow function inside a class that will inherited into instantiated object. For ex:
7. ![[Pasted image 20240715003122.png]]
8. Now check below image from google developer console, you will see the binding of functions inside a class.
9. ![[Pasted image 20240715003255.png]]
10. As you can see, the subtracts method is inside the aliceClass object however, the adds method is inside the prototype of App.
### Constructor Functions