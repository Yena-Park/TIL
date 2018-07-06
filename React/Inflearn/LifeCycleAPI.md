Constructor
-----------
* The constructor calle only once when the component initializes.

componentWillMount
------------------
* The ComponentWillMount is invoked just before monting occurs. It is called before rencer(), therefore calling setState() synchronously in this method will not trigeer an extra renderring.
```react
import React, { Component } from 'react';

class App extends Component {
  constructor(props){
    super(props); //react에서 불러온 component를 상속하는데, component가 원래 가지고 있던 생성자 함수를 먼저 호출해주려는 것.
  }
  reder(){
    return (
      <div>
        <h1> Hi, React! </h1>
      </div>
    );
  }
}

export default App;
```
