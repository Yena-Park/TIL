State
=====
- State는 내부에서 변경할 수있다.
  (변경할 때는 언제나 setState라는함수를 사용)
```javaScript
import React, { Component } from 'react';

class Counter extends Component {

  state = {
    number: 0
  }

  handleIncrease = () => {
    this.setState({
      number: this.state.number + 1
    })
  }

  handleDecrease = () => {
    this.setState({
      number: this.state.number - 1
    })
  }

  render(){
    return (
      <div>
        <h1>카운터</h1>
        <div> 값: {this.state.number} </div>
        <button>+</button>
        <button>-<button>
      </div>
    );
  }
}

export default Counter;
```
만약 handleIncrease 와 handleDecrease를 화살표가 아닌 일반 method 형태로 바꾼다면
-------------------------------------------------------------------------
```javaScript
import React, { Component } from 'react';

class Counter extends Component {

  state = {
    number: 0
  }
  
  constructor(props) {
    super(props);
    this.handleIncrease = this.handleIncrease.bind(this);
    this.handleDecrease = this.handleDecrease.bind(this);
  }

  handleIncrease() {
    this.setState({
      number: this.state.number + 1
    })
  }

  handleDecrease() {
    this.setState({
      number: this.state.number - 1
    })
  }

  render(){
    return (
      <div>
        <h1>카운터</h1>
        <div> 값: {this.state.number} </div>
        <button>+</button>
        <button>-<button>
      </div>
    );
  }
}

export default Counter;
```
