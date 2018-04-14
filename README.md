# react-button-component
A simple react button component based on styled-components with basic styles. Great when you want a quick button that looks neat enough and is yet, customizable to the heart!

![](assets/jumbotron.png?raw=true)

## Installation

```js
  yarn add react-button-component
```

## Usage
To use the Button component, simply import it into your project, and use it just like any other component!

### The base component
By default, the button has some base styles applied to make it look clean!
```js
import React, { Component } from 'react';
import Button from 'react-button-component';

class App extends Component {
  render() {
    return (
      <div className="App">
        <Button onClick={() => alert('Welcome!')}>
          Hop in!
        </Button>
      </div>
    );
  }
}

export default App;
```
Result:
![](assets/jumbotron.png?raw=true)

### Easily extend and overwrite with styled-components
The button component is styled using styled-components library, which means you the Button component is in fact, a Styled component! Now you can use `Button.extend` to extend the styles till your heart is content! For example, we can modify the default component in the above file to have a custom style matching a particular theme:
```js
import React, { Component } from 'react';
import Button from 'react-button-component';
import logo from './logo.svg';
import './App.css';

const CustomizedButton = Button.extend`
  color: #FFF;
  border: none;
  border-radius: 5px;
  background: linear-gradient(70deg, #FF5686, #FF7B9E);
  border-bottom: 5px solid #C44267;
`

class App extends Component {
  render() {
    return (
      <div className="App">
        <CustomizedButton onClick={() => alert('bonkers!')}>
          Chearful!
        </CustomizedButton>
      </div>
    );
  }
}

export default App;
```
Result:
![](assets/chear.png?raw=true)

## Created by
buoyantair

## License
MIT