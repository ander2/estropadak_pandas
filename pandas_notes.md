# Using panda to calculate rankings

* Load data from CSV
```
gbl_data = pd.read_csv('GBL.csv')
```
* Pivot columns and aggregate sum
```
point_table = gbl_data.pivot_table(index='talde_izena', columns='kategoria', values='puntuazioa', aggfunc='sum')
```
* Drop NA values and sort
```
point_table.IG.dropna().sort_values(ascending=False)
```