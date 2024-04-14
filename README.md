# Python pandas Essentials - Indexing

## Boolean Indexing
```python
# Check to see if a record in the dataset has a 'Gold' Medal
# Results will return True or False
olympic_df.Medal == 'Gold'

0         True
1        False
2        False
3         True
4        False
         ...  
29211    False
29212    False
29213    False
29214     True
29215    False
Name: Medal, Length: 29216, dtype: bool
```

```python
# Return all records of Athletes that received a Gold Medal
olympic_df[olympic_df.Medal == 'Gold']

| City   | Edition | Sport         | Discipline    | Athlete              | NOC | Gender | Event                      | Event_gender | Medal |
|--------|---------|---------------|---------------|----------------------|-----|--------|----------------------------|--------------|-------|
| Athens | 1896    | Aquatics      | Swimming      | HAJOS, Alfred        | HUN | Men    | 100m freestyle            | M            | Gold  |
| Athens | 1896    | Aquatics      | Swimming      | MALOKINIS, Ioannis   | GRE | Men    | 100m freestyle for sailors| M            | Gold  |
| Athens | 1896    | Aquatics      | Swimming      | HAJOS, Alfred        | HUN | Men    | 1200m freestyle           | M            | Gold  |
| Athens | 1896    | Aquatics      | Swimming      | NEUMANN, Paul        | AUT | Men    | 400m freestyle            | M            | Gold  |
| Athens | 1896    | Athletics     | Athletics     | BURKE, Thomas        | USA | Men    | 100m                       | M            | Gold  |
| ...    | ...     | ...           | ...           | ...                  | ... | ...    | ...                        | ...          | ...   |
| Beijing| 2008    | Wrestling     | Wrestling Gre-R | GUENOT, Steeve     | FRA | Men    | 60 - 66kg                  | M            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Gre-R | KVIRKELIA, Manuchar | GEO | Men    | 66 - 74kg                  | M            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Gre-R | MINGUZZI, Andrea    | ITA | Men    | 74 - 84kg                  | M            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Gre-R | KHUSHTOV, Aslanbek  | RUS | Men    | 84 - 96kg                  | M            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Gre-R | LOPEZ, Mijain       | CUB | Men    | 96 - 120kg                 | M            | Gold  |

```
```python
# Return all Women who received Gold Medals
olympic_df[(olympic_df.Medal == 'Gold') & (olympic_df.Gender == 'Women')]

| City   | Edition | Sport         | Discipline      | Athlete               | NOC | Gender | Event                                  | Event_gender | Medal |
|--------|---------|---------------|-----------------|-----------------------|-----|--------|----------------------------------------|--------------|-------|
| Paris  | 1900    | Golf          | Golf            | ABBOTT, Margaret Ives| USA | Women  | individual                             | W            | Gold  |
| Paris  | 1900    | Tennis        | Tennis          | COOPER, Charlotte     | GBR | Women  | mixed doubles                          | X            | Gold  |
| Paris  | 1900    | Tennis        | Tennis          | COOPER, Charlotte     | GBR | Women  | singles                                | W            | Gold  |
| St Louis| 1904    | Archery       | Archery         | HOWELL, Matilda Scott | USA | Women  | double columbia round (50y - 40y - 30y)| W            | Gold  |
| St Louis| 1904    | Archery       | Archery         | HOWELL, Matilda Scott | USA | Women  | double national round (60y - 50y)      | W            | Gold  |
| ...    | ...     | ...           | ...             | ...                   | ... | ...    | ...                                    | ...          | ...   |
| Beijing| 2008    | Weightlifting | Weightlifting   | CAO, Lei              | CHN | Women  | 75kg                                   | W            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Free. | HUYNH, Carol          | CAN | Women  | - 48kg                                 | W            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Free. | YOSHIDA, Saori        | JPN | Women  | 48 - 55kg                              | W            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Free. | ICHO, Kaori           | JPN | Women  | 55 - 63kg                              | W            | Gold  |
| Beijing| 2008    | Wrestling     | Wrestling Free. | WANG, Jiao            | CHN | Women  | 63 - 72kg                              | W            | Gold  |

```
