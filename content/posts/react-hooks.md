---
title: "React Hooks"
date: 2020-10-24T14:58:58+11:00
draft: false
---

- Hooks are  let you to use state and other React features  in stateless components(Functional)
-  Stateful logic without changing component hierarchy
- Reusable stateful logic pass between components.
- Allow you to write complex logic in functional components without the need of any Class Component.
- It can be extracted in other files, shared, reused and tested more easily
- There are 3 basic hooks  types such as

##### useState
* useState use to declare new state variable to component

```javascript
import React from 'react
import {useState} from "react"

const[count, setCount] = useState(0);
```
##### useEffect
* useEffect use to connect with component lifecycle
```javascript
import React from 'react
import {useState, useEffect} from "react"

useEffect(() =>  {
    setCount{count}
}
```

##### useContext
- useContext provides way to pass data through the component without having pass props manually at every level
- less commonly used
- can read the value 

```javascript
import React, { useContext} from "react";
import ReactDOM from "react-dom";

const newContext = React.createContext({ color: 'black' });
const value = useContext(newContext);
```

###### class component without use of hooks
```javascript
import React from "react";
import ReactDOM from "react-dom";

class App extends React.Component {
  state = {
    count: 0
  };
  setCount = () => {
    this.setState({ count: this.state.count +1})
  }
  render() {
    return (
      <React.Fragment>
        <h1>{this.state.count}</h1>
        <button onClick={this.setCount}>Click me</button>
      </React.Fragment>
    );
  }
}
export default App;
```

###### Stateless component with hooks
```javascript
import React, { useState} from "react";
import ReactDOM from "react-dom";

const App = () => {
  const[count, setCount] = useState(0);
  const increment = () => setCount(count +1);
  return (
    <React.Fragment>
      <h1>{count}</h1>
      <button onClick={increment}>Click me</button>
    </React.Fragment>
  );
}
export default App;
```
