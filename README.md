# Python pandas Essentials - Basic Analysis

## Exercise
```python
# In which events did Jesse Owens win a medal?

jo = olympics_df[olympics_df.Athlete =='OWENS, Jesse']
jo

| City   | Edition | Sport     | Discipline | Athlete     | NOC | Gender | Event         | Event_gender | Medal |
|--------|---------|-----------|------------|-------------|-----|--------|---------------|--------------|-------|
| Berlin | 1936    | Athletics | Athletics  | OWENS, Jesse| USA | Men    | 100m          | M            | Gold  |
| Berlin | 1936    | Athletics | Athletics  | OWENS, Jesse| USA | Men    | 200m          | M            | Gold  |
| Berlin | 1936    | Athletics | Athletics  | OWENS, Jesse| USA | Men    | 4x100m relay | M            | Gold  |
| Berlin | 1936    | Athletics | Athletics  | OWENS, Jesse| USA | Men    | long jump     | M            | Gold  |

```

```python
# Get the view_counts of Jesse Owens Events
jo.Event.value_counts()

Event
100m            1
200m            1
4x100m relay    1
long jump       1
Name: count, dtype: int64
```

```python
# Which country has won the most men's gold medals in singles badminton over the years?Sort the results alphabetically by the player's name.

medals = olympics_df[(olympics_df.Medal == 'Gold') & (olympics_df.Gender == 'Men') & (olympics_df.Sport == 'Badminton')]
medals

medals.sort_values(by='Athlete')
```

```python
# Which three countries have won the most medals in the recent years (from 1984 to 2008)?

rec = olympics_df[olympics_df.Edition >= 1984]
rec

rec.NOC.value_counts().head(3)
```

```python
# Display the male gold medal winners for the 100m Track & Field sprint event over the years. List the results starting with the most recent. Show the Olympic City, Edition, Athlete and the country they represent.

mgm100m = olympics_df[(olympics_df.Gender == 'Men') & (olympics_df.Medal == 'Gold') & (olympics_df.Event == '100m')]
mgm100m.sort_values(['Edition'], ascending=False)

# Select only the columns that are relevant
mgm100m.sort_values(['Edition'], ascending=False)[['City', 'Edition', 'Athlete', 'NOC']]
```


