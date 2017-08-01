# Getting-Started-with-React-Unit-Testing

A Very Simple Tutorial on getting Started with Unit Testing on React.

A simple React Component:

import React, { Component } from 'react';
//import './Card.css';

class SampleComponent extends Component {
  render() {
      return (
          <div>
            {this.props.title}
          </div>
      )    
  }
}

export default SampleComponent;

Above simple Components just renders a Label when Passed as title Props.
Sample ussage : <SampleComponent title={"This is a Title Passed as Prop"} />


We will use Enzyme to shallow Render the React Component. 

What is Enzyme ?

In General We will mutate the DOM(Manipulate the Elements on the UI ) by directly accessing the elements by Id or by Class Name,

Like in case of 
<input id="userInputField" value={userEntetedValue} />

In order to Test this Basic HTML component we will get the element by Id and apply key stroke methods on the Element(in case of Input) but in react we do not manipulate the DOM directly but instead React takes care of manipulating the DOM by running a series of algorithems to mazimize the effieciency.


All that Apart, We are here to Rest our React Component and We should able to Control each and every part of it. But when When Rendered on DOM React becomes pure HTML, which yields back to above case of testing direct Dom Elements and we can have to abilitu to the React Component(there is no longer a State or component Life Cycles here) But instead we need to test the React Components even before they are written to DOM(Kind of), So Enzyme helps to take a Copy of the React Component and Play on it.

All the React Component API's like setState(),this.props, and all life cycle methods are avaialble on the Copy. Enzyme have Rich API's that help us to play with each and everyt part of React Component and Check How it Behaves("Unit Testing: How Unit Behaves") 
