---
title: "Component types in React"
date: 2020-10-24T09:43:33+11:00
draft: false
---

* There are mainly two types of components in react
* Such as class components and functional components.Sometimes known as state or stateless components
* Components are reusable properties and return JSX. Browsers cannot read JSX. Babel helps to convert JSX to HTML

#### Functional Component
This is the way to declare functional component in react  and return JSX element

```javascript
import React from "react";
const App = () => {
  return (
    <div>
      App
    </div>
  );
};
export default App;
```

- This is the way to  pass data from parent to child through props. 
```javascript
import React from 'react'
// pass props
const Name = (props) =>{
  return (
    <div>
      Name{props.name}
    </div>);
}
export default Name;
```

```javascript
import React from 'react'
// using object destructuring
const Name = ({ name }) =>{
  return (
    <div>
      My name is: {name}
    </div>);
}
export default Name;
```

#### Class Component
- This is the way to declare class component in react  and return JSX element.
- we use (this.props)to pass data from parent to child. state and lifecycle methods also introduce to class components

```javascript
import React from "react";

class MyComponent extends React.Component {
  componentDidMount(){
   }
  constructor() {
    super();
    this.state = {
      name: "Danny",
    };
  }
  render() {
    return (
      <div>
        <h1>Hello {this.state.name}</h1>
      </div>
    );
  }
}
export default MyComponent;
```
  

