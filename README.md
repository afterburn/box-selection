# Box Selection
![](https://img.shields.io/npm/v/box-selection.svg) ![](https://img.shields.io/npm/dt/box-selection.svg)

Small JavaScript library for making box selections on HTML elements.
Makes use of CSS transforms so there is no paint flashing.
![](https://raw.githubusercontent.com/afterburn/box-selection/master/box-selection.gif)

#### Installation
```bash
npm install --save box-selection
```

#### Usage
```javascript
const instance = new BoxSelection({
  container: document.getElementById('container'), // The scope in which BoxSelection should function.
  itemSelector: '.item', // The CSS class BoxSelection will use to target items.
  selectedClass: '.selected', // The CSS class that will be added to the HTML elements that fall within the selection box.
  selectionClass: '.selection', // The CSS class that will be added to the selection box.
  mode: 'loose', // 'loose' or 'strict'
  onSelectionChange: (selectedItems) => {
    console.log(selectedItems) // Array of HTML elements that fall within the selection box.
  }
})

instance.unbind() // Function you can call to unbind all of BoxSelection's events.
```

#### Customization
CSS styling used in GIF:
```
.selection {
	background-color: rgba(255, 165, 0, 0.5);
	border: 1px solid darkorange;
	z-index: 1;
}
``