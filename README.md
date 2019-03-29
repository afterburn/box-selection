# Box Selection
![](https://img.shields.io/npm/v/box-selection.svg) ![](https://img.shields.io/npm/dt/box-selection.svg)

Small library for making box selections on HTML elements in JavaScript.

#### Installation
```bash
npm install --save box-selection
```

#### Usage
```javascript
const instance = new BoxSelection({
  container: document.getElementById('container'), // The scope in which BoxSelection should function.
  itemSelector: '.item', // The css class BoxSelection will use to target items.
  selectedClass: '.selected', // The css class that will be added to the HTML elements that fall within the selection box.
  mode: 'loose', // 'loose' or 'strict'
  onSelectionChange: (selectedItems) => {
    console.log(selectedItems) // Array of HTML elements that fall within the selection box.
  }
})

instance.unbind() // Function you can call to unbind all of BoxSelection's events.
```