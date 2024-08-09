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