# Reading Notes - 301

# Controlled Components:

The React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”. For example, if we want to make the previous example log the name when it is submitted, we can write the form as a controlled component:

```
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {    this.setState({value: event.target.value});  }
  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
# The Conditional Ternary Operator

### Here's an Object:
```
let person = {
  name: 'tony',
  age: 20,
  driver: null
};
```
We want to test if the age of our person is greater than or equal to 16. If this is true, they’re old enough to drive and driver should say 'Yes'. If this is not true, driver should be set to 'No'. We could use an if statement to accomplish this:
```
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
```
But what if I told you we could do the same exact thing in just one line of code? Well, here it is:
`person.driver = person.age >=16 ? 'Yes' : 'No';`
### Here’s what you need to know:
The `condition` is what you’re actually testing. The result of your condition should be `true` or `false` or at least coerce to either boolean value.
A `?` separates our conditional from our *true* value. Anything between the `?` and the `:` is what is executed if the `condition` evaluates to *true.*
Finally a `:` colon. If your condition evaluates to *false,* any code after the colon is executed.
