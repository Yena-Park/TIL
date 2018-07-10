```react
import React, { Component } from 'react';

class PhoneForm extends Component {

  state = {
    name: '',
    phone: '',
  }

  handleChange = (e) => {
    this.setState({
      name: e.target.value {/*"This is for that there is only one input". when event is created, value of name will be changed*/}
      [e.target.name]: e.target.value {/*There are 2 event which is for name and phone.*/}
    });
  }
  render() {
    return (
      <form>
        <input 
        name="name" 
        placeholder="Name" 
        onChange={this.handleChange} 
        value={this.state.name}
        /> {/*When the value of input is changed, the value of name will be changed. And 'placeholder' shows the default value when there's no input*/}
        <input 
        name="phone" 
        placeholder="Phone Number" 
        onChange={this.handleChange
        value={this.state.phone}
        />
        {this.state.name} {/*it will shows the name of input*/}
        {this.state.phone} {/*it will shows the phone of input*/}
      </form>
    );
  }
}

export default PhoneForm;
```
