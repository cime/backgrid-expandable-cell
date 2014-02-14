backgrid-expandable-cell
========================

Backgrid.js expandable cell extension. Works with Boostrap 3.0 out of the box.

# Configuration

```
accordion: true, //collapse all expanded rows before expanding clicked one
toggle: '<i style="cursor: pointer;" class="glyphicon toggle pull-left"></i>',
toggleClass: 'toggle',
toggleExpandedClass: 'glyphicon-minus-sign',
toggleCollapsedClass: 'glyphicon-plus-sign',
trClass: 'expandable',
tdClass: 'expandable-content'
```

# Example

```
var collection = /* your Bacbone collection */;

var columns: [
  {
    cell: Backgrid.ExpandableCell,
    accordion: false,
    expand: function (el, model) {
    
      /* set expanded row's content */
      $(el).append($('<div>').html('Content of expanded column'));
      
    }
  },
  /* other Backgrid.js columns here */
];`

var grid = new Backgrid.Grid({
  columns: columns,
  collection: collection,
  className: 'backgrid table table-striped table-bordered table-hover'
});
```
