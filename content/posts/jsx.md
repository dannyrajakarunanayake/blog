---
title: "Jsx"
date: 2020-10-24T15:04:28+11:00
draft: false
author: Danny
---

JSX looks like Javascript but start with **const** and end with ; here is the example

```javascript
import React from 'react';

const element = <h1>Hello</h1>;
```
* when you code in html it's like this 
```html
<h1>Hello</h1>
```

* JSX is syntax extension for javascript
* Written in React
* Browser can not understand JSX so it's convert into javascript through babel compiler
* After compiling JSX it's treat as javascript 
* JSX is an extension of the JavaScript language on ES6
* With JSX you can write expressions inside curly braces { }

```javascript
import React from 'react';


const element = <h1>React is {5 + 5} times better with JSX</h1>;
```


