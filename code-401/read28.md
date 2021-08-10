# RecyclerView
## Create dynamic lists with RecyclerView

RecyclerView library dynamically creates the elements, and recycles those individual elements. When an item scrolls off the screen, RecyclerView doesn't destroy its view. Instead, RecyclerView reuses the view for new items that have scrolled onscreen.

**Key classes**
1. `RecyclerView` is the `ViewGroup` that contains the views corresponding to your data.
2. Each individual element in the list is defined by a view holder object. You define the view holder by extending `RecyclerView.ViewHolder`.
3. The `RecyclerView` requests those views, and binds the views to their data, by calling methods in the adapter. You define the adapter by extending `RecyclerView.Adapter`.
4. Layout managers are all based on the library's `LayoutManager` abstract class.

**Steps for implementing your RecyclerView**
1. Decide what the list or grid is going to look like.
2. Design how each element in the list is going to look and behave. Based on this design, extend the `ViewHolder` class.
3. Define the Adapter that associates your data with the ViewHolder views.

**Plan your layout**
The RecyclerView library provides three layout managers:
- `LinearLayoutManager` arranges the items in a one-dimensional list.
- `GridLayoutManager` arranges all items in a two-dimensional grid, vertically and horizontally.
- `StaggeredGridLayoutManager` arranges all items  in a row or column can end up offset from each other.

**Implementing your adapter and view holder**
`Adapter` and `ViewHolder` work together to define how your data is displayed. 

When you define your adapter, you need to override three key methods:
- `onCreateViewHolder()`: `RecyclerView` calls this method whenever it needs to create a new `ViewHolder`. 
- `onBindViewHolder(`): `RecyclerView` calls this method to associate a `ViewHolder` with data. 
- `getItemCount()`: `RecyclerView` calls this method to get the size of the data set.