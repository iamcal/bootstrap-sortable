# bootstrap-sortable

Make any bootstrap table sortable. Also works for non-bootstrap tables. Pretty badly named.


## Usage

* Add references to `bootstrap-sortable.css` and `bootstrap-sortable.js` to your page.
* Add `class="sortable"` to any table you want to sort.
  * Your table *must* have a `<thead>` element around the header.
* If you add new tables or rows run-time, call `$.bootstrapSortable()` to activate the new elements.

## More Options

You can choose a single column to be sorted when table is first loaded:


	<th>Column 1</th>
	<th>Column 2</th>
	<th data-defaultsort="desc">Column 3</th>


For columns that should no be initially sorted, you can choose the sort order to be used the first time they are clicked:

	<th data-defaultorder="asc">Column 1</th>
	<th data-defaultorder="asc">Column 2</th>
	<th data-defaultorder="desc">Column 3</th>

If you don't specify, the first click will sort ascending.

If you are using `rowspan` or `colspan` properties in your header, you can override which column each header sorts.

	<th>First Column</th>
	<th colspan="3" data-sortkey="2">Next 3 columns</th>

The column indexes start at zero.

To disable a header from allowing sorting, add a CSS class:

	<th>Column 1</th>
	<th class="no-sort">Column 2</th>
	<th>Column 3</th>

If you want to sort based on something other than the contents of the cell, you can add an extra attribute:

	<td data-value="4723">4,723</td>
	<td data-value="0"><i>none</i></td>
