## Binding this keyword in a class
1. In a event handler when we do like this onClick = {this.addNums} and if we try to console.log this.state inside of that addNums function, it won't work. We need to find this to addNum, onClick = {this.addNums.bind(this)} in order for this to work
2. Next is we can also add the above bind function directly inside the constructor that also works.
3. If we do not want to bind and all, just create a constructor function of addNums and that automatically binds this to addNums.