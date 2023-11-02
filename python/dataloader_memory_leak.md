# tqdmなどがPytorchのDataloaderのメモリリークに繋がる

**追記：tqdmに関しては[ここ](https://github.com/neuralmagic/sparseml/pull/153)で修正されたっぽい**
(cycleは相変わらずダメ)

参考：[tqdmでメモリリークにハマった話（機械学習）](https://qiita.com/nanoseeing/items/72df19278377002cd881)

```python
from tqdm import tqdm

tqdm(loader)             # ダメ
enumerate(tqdm(loader))  # ダメ
tqdm(enumerate(loader))  # OK
```

cycleとかもダメ
```python
from itertools import cycle

cycle(loader) # ダメ
```