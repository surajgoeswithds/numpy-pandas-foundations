# NumPy & Pandas Foundations

Daily practice and notebooks for learning NumPy and Pandas, part of a structured 50-day data science sprint.

## Progress

### NumPy Complete ✅
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
- [ ] Data Transformation
- [ ] Melt and Pivot
- [ ] Aggregation & Grouping
- [ ] Merging & Joining Data
- [ ] Working with CSVs

### Kaggle Pandas Micro-course — In progress (1/6 exercises)
- [x] Exercise 1: Creating, Reading and Writing
- [x] Exercise 2: Indexing, Selecting & Assigning
- [ ] Exercise 3: Summary Functions and Maps
- [ ] Exercise 4: Grouping and Sorting
- [ ] Exercise 5: Data Types and Missing Values
- [ ] Exercise 6: Renaming and Combining

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
- `exercise-creating-reading-and-writing.ipynb` — Kaggle Exercise 1: DataFrame/Series creation, read_csv with index_col, to_csv
- `exercise-indexing-selecting-assigning.ipynb` — Kaggle Exercise 2: .loc/.iloc, fancy indexing with lists, boolean masking, multi-condition filtering with &/| precedence

## Notes
- Slicing returns a *view*, not a copy — `arr` and a slice `b = arr[...]` share the same underlying memory.
- Broadcasting rule: shapes are compared from the right; dimensions must be equal or one of them must be 1.
- Axis position matches `.shape` index — `axis=0` collapses rows (`.shape[0]`), `axis=1` collapses columns (`.shape[1]`).
- `.query()` returns a copy, not a view — filtered results are a new DataFrame; changes don't affect the original unless reassigned.