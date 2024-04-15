# Python pandas Essentials - Indexing

## Using loc[]
```python
odf.loc['BOLT, Usain']

KeyError: 'BOLT, Usain'
```

```python
# No error
odf.set_index('Athlete', inplace=True)
odf.loc['BOLT, Usain']
```