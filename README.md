### blaze
---
https://github.com/blaze/blaze

```py
import blaze as bz
iris = bz.Data('postgresql://localhost::iris')
iris

iris.species.distinct()
bz.by(iris.species, smallest=iris.petal_length.min(),
  largest=iris.petal_length.max())
  
accounts = Symbol('accounts', 'var * {id: int, name: string, amount: }')  
deadbeats = accounts[accounts.amount < 0].name

L = [[1, 'Alice', 100],
  [2, 'Bob', -200],
  [3, 'Charlie', 300],
  [4, 'Denis', 400],
  [5, 'Edith', -500]]

list(compute(deadbeats, L))

df = DataFrame(L, columns=['id', 'name', 'amount'])
compute(deadbeats, df)
```

```sh
conda install blaze
pip install blaze
conda install blaze -c blaze
pip install http://github.com/blaze/blaze --upgrade
conda install blaze spark -c blaze -c anaconda-cluster -y
conda remove odo blaze blaze-core datashape -y
```

```
```


