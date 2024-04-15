# Python pandas Essentials - Indexing

## set_index()
```python
# Set the new index to a variable 'athlete'
athlete = odf.set_index('Athlete')
athlete.head()
```

```python
# Reset to original index
athlete.reset_index(inplace=True)
athlete.head()
```