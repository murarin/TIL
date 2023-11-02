# PythonコードのRAMの使用率を確認する

実行しているPythonコードがどれくらいRAMを消費しているか確認できる。 \
下記のコードを挿入すると、その時点でのメモリ使用率がPrintされる。\
使用例：メモリリーク箇所の特定など

```python
import psutil

process = psutil.Process(os.getpid())
print(process.memory_info().rss)  # バイト単位での常駐セットサイズ（RSS）
```