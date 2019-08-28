### Remember

Answer these on your own, then compare answers as a group

1.  What is React?

<!-- React is a JS library that allows us to condense functionality into attachable components. In other words, it gives you the ability to make custom HTML tags, that will render whatever HTML and Javascript you need to, in one callable tag. -->

2.  What is create-react-app?

<!-- CRA ("I'm getting tried of having to write it oput every time) is a boilerplate generator for React. Running CRA will generate the basic folder/file structure you need to make an app, along with the basic files to get started. In other words, its like how some code editors will include boilerplate code when you create a new file. -->
3.  What is Component Based Architecture?
<!-- The "lego blocks" of React. You code in the functionality you want to the component, and then you can call the component as you want it in the main app.js -->
4.  What is JSX?
<!-- JSX is the language of react, and allows us to store data with html tags at the same time.
const element = <h1>Hello, World!</h1> -->

5.  What is the virtual DOM?
<!-- The VDOM is a virtual copy of DOM, which is what is edited by React using your code. Once all the changes are made to the VDOM, the VDOM updates the live DOM, only changing what has been updated. This has the benefit of being faster than editing the live DOM directly, since unchanged portions of the page aren't reloaded. -->

6.  What is unidirectional (one-way) data flow?
<!-- It is exactly what it sounds, data can only go in one direction. Data can only be passed from the parent to child to parent, but can't be accessed by another child of the parent. -->

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
<!-- CRA creates the boilerplate code and file structure needed to start a react-app, under the name specified. Every you need to render an app is availble at the start - all you need to do is add any extra functionailty you are looking for. -->

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
