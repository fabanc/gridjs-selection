# gridjs-selection

## Description

This plugin is designed for [gridjs](https://github.com/grid-js/gridjs). The goal of this plugin is two offer more both single-row selection and multiple-rows selection.

## Examples

In HTML, you must first load the plugin and gridjs, as the plugin depends on it.

```html
<script src="js/gridjs.umd.js"></script>
<script src="js/gridjsselection.umd.js"></script>
```

### Single Row Selection Plugin

```javascript
    let singleSelection = gridjsSelection.RowSelectionSingle;
    let grid = new gridjs.Grid({
        columns: [
            {
                id: 'select',
                name: 'Select',
                plugin: {
                    component: singleSelection
                }
                },
                {
                id: 'a',
                name: 'Column A'
                },
                {
                id: 'b',
                name: 'Column B'
                },
                {
                id: 'c',
                name: 'Column C'
                }
            ],
        data: [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9],
            [10, 11, 12],
        ],
        }).render(document.getElementById("mygrid"));

        grid.on('rowClick', (...args) => console.log('row: ' + JSON.stringify(args), args));
        grid.on('cellClick', (...args) => console.log('cell: ' + JSON.stringify(args), args));
```
### 