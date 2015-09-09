# Level 5. 控制元件
這是 React 系列教學中的簡易範例 TodosApp


## 本階段目標
1. 新增 Input 元件，讓使用者可以登打新的待辦事項
2. 在 App 元件中，使用 State 來儲存待辦事項
3. 在 App 元件中，加入處理新增待辦事項的邏輯，並更改 State


## 你可以在這階段學習
### JS
1. [Function.prototype.bind()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind)

### React
1. [Components are Just State Machines](https://facebook.github.io/react/docs/interactivity-and-dynamic-uis.html#components-are-just-state-machines)
2. [Controlled Components](https://facebook.github.io/react/docs/forms.html#controlled-components)
```js
class Input extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: '' };
  }
  handleChange(evt) {
    this.setState({ value: evt.target.value });
  }
  render() {
    return (
      <input
        type="text"
        value={this.state.value}
        onChange={this.handleChange.bind(this)} />
    );
  }
}
```

