# Numpy

1. **NumPy**是[Python語言](https://zh.wikipedia.org/wiki/Python)的一個擴充程式庫。支援高階大規模的[多維](https://zh.wikipedia.org/wiki/%E7%B6%AD%E5%BA%A6)[陣列](https://zh.wikipedia.org/wiki/%E9%99%A3%E5%88%97)與[矩陣](https://zh.wikipedia.org/wiki/%E7%9F%A9%E9%99%A3)運算，此外也針對陣列運算提供大量的[數學](https://zh.wikipedia.org/wiki/%E6%95%B8%E5%AD%B8)[函式](https://zh.wikipedia.org/wiki/%E5%87%BD%E6%95%B8)[函式庫](https://zh.wikipedia.org/wiki/%E5%87%BD%E5%BC%8F%E5%BA%AB)。

### 2. **ndarray 資料結構:** NumPy的核心功能是ndarray（即*n*-dimensional array，多維陣列）資料結構。這是一個表示多維度、同質並且固定大小的陣列物件。

### 3. **局限性:** 在陣列中插入或追加元素並不像Python的list一樣簡單。

`np.pad(...)`實際上建立了新的具有目標形狀和填充值的陣列，將給定陣列的值複製到新陣列中並返回新陣列。`np.concatenate([a1,a2])`並沒有直接連接兩個陣列，而是返回新的陣列，該陣列填充了兩個原陣列的值。用`np.reshape(...)`改變陣列的維度只有在陣列中元素數量不變的情況下才能實現。造成以上情況的原因是NumPy的陣列必須占用連續的記憶體空間。

1. 未經向量化的演算法通常執行緩慢，因為它們必須用純Python方法實現。
2. 可與NumPy整合的開源解決方案包括 numexpr[[17]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-17)和[Numba](https://zh.wikipedia.org/wiki/Numba)[[18]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-18)。Cython和Pythran是靜態編譯的解決方案。
3. 許多現代大型科學計算應用的要求超出了NumPy陣列的能力。例如，NumPy陣列通常載入到電腦的記憶體中，然而記憶體可能沒有足夠的容量；此外，NumPy僅在單個[CPU](https://zh.wikipedia.org/wiki/%E4%B8%AD%E5%A4%AE%E5%A4%84%E7%90%86%E5%99%A8)上進行操作，而許多線性代數算子可以通過CPU的叢集和其它特殊硬體（例如[GPU](https://zh.wikipedia.org/wiki/%E5%9C%96%E5%BD%A2%E8%99%95%E7%90%86%E5%99%A8)、[TPU](https://zh.wikipedia.org/wiki/%E5%BC%A0%E9%87%8F%E5%A4%84%E7%90%86%E5%8D%95%E5%85%83)，部分深度學習應用也依賴於這些特殊硬體）來加速。
4. 因此，近期在Python的生態中出現了許多其它工具，例如用於分散式陣列的[Dask](https://zh.wikipedia.org/w/index.php?title=Dask&action=edit&redlink=1)、用於GPU計算的[TensorFlow](https://zh.wikipedia.org/wiki/TensorFlow)和JAX[[19]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-19)等。這些庫通常實現或模仿NumPy的部分[API](https://zh.wikipedia.org/wiki/%E5%BA%94%E7%94%A8%E7%A8%8B%E5%BA%8F%E6%8E%A5%E5%8F%A3)，因此使用者不需大量改動就可以部署原先使用NumPy的程式。[[20]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-Nature-20)近期出現的由Nvidia的CUDA架構加速的[CuPy](https://zh.wikipedia.org/w/index.php?title=CuPy&action=edit&redlink=1)庫[[21]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-21)展示了快速計算的潛力，是NumPy的直接替代品。[[22]](https://zh.wikipedia.org/zh-tw/NumPy#cite_note-22)
