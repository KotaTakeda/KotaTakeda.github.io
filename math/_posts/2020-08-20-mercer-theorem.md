---
layout: post
title:  "Mercerの定理"
description: "Mercerの定理の紹介と応用"
date:   2020-08-20 15:54:00 +0900
dir: /math/
tag: '機械学習'
---
### 目次
- [Key word](#key-word)
- [導入](#導入)
- [Mercer kernel](#mercer-kernel)
- [Mercerの定理](#mercerの定理)
- [定理の応用](#定理の応用)
- [参考](#参考)

### Key word
- 統計: カーネルトリック，SVM，PCA
- 数学: スペクトル理論，Karhunen-Loeve展開

### 導入
積分核として積分作用素を定めたり，内積を与えたりする2変数関数(kernel)の展開についての定理を簡単に紹介します．

Hilbert Schmidtの理論から$L^2$展開できますが，連続性や半正定値性から一様収束が導かれるのがポイントです．

### Mercer kernel
以下の３つの性質を満たすkernelをMercer kernelという．
- 連続
- 対称
- 半正定値

### Mercerの定理
Mercer kernel $ K $に対して$ x \mapsto K(x,x) \in L^1 $が成り立つとき

$$
  K(x,y) = \sum_{n} \lambda_n \psi_n(x) \psi_n(y)
$$


と絶対一様展開できる．

#### 証明
[pdfリンク](/math/pdf/chapter11.pdf)
### 定理の応用
#### カーネルトリック
1. SVMでよく使われるカーネル[^kernels]はMercer kernelの条件を満たすので高次元特徴空間でのデータの内積をカーネルで置き換えることができる．
2. これによって計算量をそれほど増やすことなく特徴空間を高次元へ拡張することができる．

#### その他
- Karhunen-Loeve展開の収束を示す際に使います．
- また，離散的なKarhunen-Loeve展開としてPCAを解釈できます．

### 参考
pdfリンクにあります．

### 注意
[^kernels]: 多項式カーネルやガウシアンカーネル，シグモイドカーネルなど．
