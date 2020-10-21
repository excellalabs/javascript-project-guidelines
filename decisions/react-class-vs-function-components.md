# React Class vs. Function Components

React allows you to write your components as ES6 classes or plain JavaScript functions.

### Class component:

```javascript
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

### Function component:

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

Both options are valid React syntax, so it is beneficial to understand both. However, we recommended choosing to write function components over class components going forward.

## Why

With the introduction of the [`useState`](https://reactjs.org/docs/hooks-state.html) and [`useEffect`](https://reactjs.org/docs/hooks-effect.html) hooks, function components can manage their own state and lifecycle behavior like class components. Therefore, both approaches are functionally equivalent.

For all new projects and new components, we recommend writing function components because of their simple syntax and behavior out of the box. You can then deliberately choose to add state or lifecycle with hooks if needed.
