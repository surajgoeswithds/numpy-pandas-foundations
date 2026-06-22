# NumPy & Pandas Foundations

Daily practice and notebooks for learning NumPy and Pandas, part of a structured data science sprint.

## Progress

### NumPy 
- [x] Why use NumPy (cache locality, memory layout, vectorization)
- [x] Creating NumPy Arrays
- [x] Indexing and Slicing
- [x] Multidimensional Indexing and Axis
- [x] Data Types in NumPy
- [x] Broadcasting in NumPy
- [x] Built-in Mathematical Functions

### Pandas 
- [x] Getting Started with Pandas
- [x] Core Data Structures in Pandas
- [x] Creating DataFrames
- [x] Data Selection & Filtering
- [x] Data Cleaning & Preprocessing
- [x] Data Transformation
- [x] Melt and Pivot
- [x] Aggregation & Grouping
- [x] Merging & Joining Data
- [x] Working with CSVs

### Kaggle Pandas Micro-course 
- [x] Exercise 1: Creating, Reading and Writing
- [x] Exercise 2: Indexing, Selecting & Assigning
- [x] Exercise 3: Summary Functions and Maps
- [x] Exercise 4: Grouping and Sorting
- [x] Exercise 5: Data Types and Missing Values
- [x] Exercise 6: Renaming and Combining

## Notebooks
- `Numpy vs Python.ipynb` — speed/memory comparison, cache locality demo
- `Creating_numpy_arrays.ipynb` — array creation methods (`np.array`, `zeros`, `ones`, `full`, `eye`, `arange`, `linspace`), shape/size/dtype, reshaping & flattening
- `Indexing & slicing.ipynb` — basic indexing, slicing, views vs copies, fancy indexing, boolean masking
- `Multidimensional indexing.ipynb` — axis operations, 2D/3D indexing and slicing
- `Numpy Data Types.ipynb` — dtype conversion, upcasting/downcasting, complex numbers
- `Broadcasting.ipynb` — broadcasting rules, vectorized stats, normalization
- `Basic questions.ipynb` — self-solved practice problems applying the above concepts
- `Getting Started with Pandas.ipynb` — Series, DataFrame creation, index/columns
- `Creating DataFrames.ipynb` — DataFrame from list/dict/NumPy array, reading Excel/CSV/URL data, EDA basics (`head`, `tail`, `info`, `describe`, `columns`, `shape`)
- `Data Selection & Filtering.ipynb` — `.loc`/`.iloc`/`.at`/`.iat`, boolean masking, `.query()` with chained/multi-conditions, copy vs view in filtering
- `Data Cleaning & Preprocessing.ipynb` — missing data (`isnull`, `dropna`, `fillna`, `ffill`/`bfill`), duplicates (`duplicated`, `drop_duplicates`, subset-based), `.str` methods, dtype fixing (`astype`), `.apply()`/`.map()`/`.replace()` for transformations
- `Data Transformation.ipynb` — sort_values(), reset_index() with inplace/drop, column reordering via df[[col_order]]
- `Melt and Pivot.ipynb` — pd.melt() for wide-to-long, pivot_table() for long-to-wide, reshaping DataFrames
- `Aggregation and Grouping.ipynb` — groupby(), agg(), transform(), aggregate functions on grouped data
- `Merging and Joining.ipynb` — merge(), join(), concat(), inner/outer/left/right joins
- `exercise-creating-reading-and-writing.ipynb` — Kaggle Exercise 1: DataFrame/Series creation, read_csv with index_col, to_csv
- `exercise-indexing-selecting-assigning.ipynb` — Kaggle Exercise 2: .loc/.iloc, fancy indexing with lists, boolean masking, multi-condition filtering with &/| 
- `exercise-summary-functions-and-maps.ipynb` — Kaggle Exercise 3: median, unique, value_counts, idxmax, str.contains, apply with row-wise logic, mean-centering
- `exercise-grouping-and-sorting.ipynb` — Kaggle Exercise 4: groupby, size, agg with multiple functions, sort_values, sort_index, MultiIndex grouping
- `exercise-data-types-and-missing-values.ipynb` — Kaggle Exercise 5: dtype inspection, astype() conversion, isnull()/sum() for null detection, fillna(), value_counts(), sort_values()
- `exercise-renaming-and-combining.ipynb` — Kaggle Exercise 6: rename(columns=), rename_axis(index=''), pd.concat([]), set_index().join() for merging on a shared key

## Notes
- Slicing returns a *view*, not a copy — `arr` and a slice `b = arr[...]` share the same underlying memory.
- Broadcasting rule: shapes are compared from the right; dimensions must be equal or one of them must be 1.
- Axis position matches `.shape` index — `axis=0` collapses rows (`.shape[0]`), `axis=1` collapses columns (`.shape[1]`).
- `.query()` returns a copy, not a view — filtered results are a new DataFrame; changes don't affect the original unless reassigned.