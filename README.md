# NumPy & Pandas Foundations

Daily practice and notebooks for learning NumPy and Pandas, part of a structured science sprint.

## Progress

### NumPy (CWH Section 5)
- [x] Why use NumPy (cache locality, memory layout, vectorization)
- [x] Creating NumPy Arrays
- [x] Indexing and Slicing
- [ ] Multidimensional Indexing and Axis
- [ ] Data Types in NumPy
- [ ] Broadcasting in NumPy
- [ ] Built-in Mathematical Functions

## Notebooks
- `Creating_numpy_arrays.ipynb` — array creation methods (`np.array`, `zeros`, `ones`, `full`, `eye`, `arange`, `linspace`), shape/size/dtype, reshaping & flattening
- `Indexing & slicing.ipynb` — basic indexing, slicing, views vs copies, fancy indexing, boolean masking
- `Basic questions.ipynb` — self-solved practice problems applying the above concepts

## Notes
Slicing returns a *view*, not a copy — `arr` and a slice `b = arr[...]` share the same underlying memory.