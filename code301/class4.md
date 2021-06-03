## React and Forms

### Forms
- HTML form elements work differently from other DOM elements in React, because form elements keep some internal state. 

```
<form>
  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>
```

### Controlled Components
[source](https://reactjs.org/docs/forms.html)
- In HTML form elements such as <input>, <textarea>, and <select> maintain their own state and update based on user input.
- In React, mutable state is kept in state property components and updated with setState()

```
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
- Since value attribute is set on the form element, the displayed value will stay this.state.value, React state the source truth.

[<== Back](README.md)