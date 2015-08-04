# An ES6-friendly on-click-outside React component.

This is a React component that can be used to listen for clicks outside of a given component.  As an example, you may need to hide a menu when a user clicks elsewhere on the page.

This component was created specifically to support ES6-style React components.  If you want to use a mixin instead, I would recommend the [react-onclickoutside](https://github.com/Pomax/react-onclickoutside) mixin.

## Installation

```
npm install react-onclickout --save
```

## Usage

There are two ways to use this component.

### As a wrapper component

```jsx
let ClickOutHandler = require('react-onclickout');

class ExampleComponent extends React.Component {

  onClickOut(e) {
    alert('user clicked outside of the component!');
  }

  render() {
    return (
      <ClickOutHandler onClickOut={this.onClickOut}>
        <div>Click outside of me!</div>
      </ClickOutHandler>
    );
  }
}
```

### As a base component

```jsx
let ClickOutComponent = require('react-onclickout');

class ExampleComponent extends ClickOutComponent {

  onClickOut(e) {
    alert('user clicked outside of the component!');
  }

  render() {
    return (
      <div>Click outside of me!</div>
    );
  }
}
```

That's pretty much it.  Pull requests are more than welcome!
