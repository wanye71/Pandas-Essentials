# Python pandas Essentials - Indexing

## Index
```python
type(odf.index)
pandas.core.indexes.range.RangeIndex

odf.index[100] = 5

---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
Cell In[5], line 1
----> 1 odf.index[100] = 5

File ~\anaconda3\Lib\site-packages\pandas\core\indexes\base.py:5348, in Index.__setitem__(self, key, value)
   5346 @final
   5347 def __setitem__(self, key, value) -> None:
-> 5348     raise TypeError("Index does not support mutable operations")

TypeError: Index does not support mutable operations
```