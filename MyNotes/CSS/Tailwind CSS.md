1. Installation
	1. `npm install -D tailwindcss postcss autoprefixer`
2. tailwind.config.js file
	1. This file has all the configuration of tailwind css project. Check below
```
	npx tailwindcss init -p

	- Alright so, npx is a package runner tool. Incase we don't want to install the whole package or if the package is not installed and we want a specific component from a particular library we can extract that using npx.
	- The init command is used to initialize the tailwind.config.js file where we specify all the styles and configurations like themes, designs etc.
	- -p command is used to specify to also initalize postcss.config.js file since tailwind relies on postcss to transform the css.
```
3. The app.css file
	1. We need to include below three lines in our root css file of React Application.
```
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
```

