### Remember

Answer these on your own, then compare answers as a group

1.  What is state?

<!-- State is the "bottled" data created inside of the constructor. Similar to creating a variable in normal JS, this data is arranged in such a way that we can pass it to child components. -->
2.  Where do you set initial state?
<!-- In App.js, with the base data needed to start building functionality. -->

3.  What method do you use to update state?
<!-- this.setstate({propertyname: value}) -->

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.
<!-- LeadMentor is called within App.js, and extends from Component in react.
When LeadMentor is called, the properties it is called with are passed in, similar to how a funciton can be called with arguments being passed in. A new value of questionsAnswered is created as a property within LeadMentor's state. The handleClick function updates questionsAnswered by increasing it by one whenever it is called. Finally, this class renders a div containing the mentor's name, how many questions they have answered today, and a button that increases the number of questions answered. -->

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.

### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?