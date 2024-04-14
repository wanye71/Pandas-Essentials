# Python pandas Essentials - Indexing

## String Handling
```python
# Find all records where the Athlete name 'Florence' is True
olympic_df[olympic_df.Athlete.str.contains('Florence')]

| City                  | Edition | Sport     | Discipline      | Athlete                        | NOC | Gender | Event                     | Event_gender | Medal  |
|-----------------------|---------|-----------|-----------------|--------------------------------|-----|--------|---------------------------|--------------|--------|
| London                | 1908    | Skating   | Figure skating  | SYERS, Florence                | GBR | Women  | individual                | W            | Gold   |
| London                | 1908    | Skating   | Figure skating  | SYERS, Florence                | GBR | Women  | pairs                     | X            | Bronze |
| Paris                 | 1924    | Aquatics  | Swimming        | BARKER, Florence               | GBR | Women  | 4x100m freestyle relay   | W            | Silver |
| Helsinki              | 1952    | Athletics | Athletics       | FOULDS-PAUL, June Florence    | GBR | Women  | 4x100m relay             | W            | Bronze |
| Melbourne / Stockholm | 1956    | Athletics | Athletics       | FOULDS-PAUL, June Florence    | GBR | Women  | 4x100m relay             | W            | Silver |
| Tokyo                 | 1964    | Athletics | Athletics       | AMOORE-POLLOCK, Judith Florence | AUS | Women  | 400m                      | W            | Bronze |
| Los Angeles           | 1984    | Athletics | Athletics       | GRIFFITH-JOYNER, Florence      | USA | Women  | 200m                      | W            | Silver |
| Seoul                 | 1988    | Athletics | Athletics       | GRIFFITH-JOYNER, Florence      | USA | Women  | 100m                      | W            | Gold   |
| Seoul                 | 1988    | Athletics | Athletics       | GRIFFITH-JOYNER, Florence      | USA | Women  | 200m                      | W            | Gold   |
| Seoul                 | 1988    | Athletics | Athletics       | GRIFFITH-JOYNER, Florence      | USA | Women  | 4x100m relay              | W            | Gold   |
| Seoul                 | 1988    | Athletics | Athletics       | GRIFFITH-JOYNER, Florence      | USA | Women  | 4x400m relay              | W            | Silver |
```

```python

```
