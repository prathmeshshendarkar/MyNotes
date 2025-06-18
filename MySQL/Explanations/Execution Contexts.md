## Execution Contexts
1. Whenever we write any command using select operator and fetch something from a table the order of execution is from right side.
2. For ex: If we have a query like `SELECT column1 FROM TABLE1`
	1. First `FROM TABLE1` will execute then
	2. `SELECT column1` will be executed.