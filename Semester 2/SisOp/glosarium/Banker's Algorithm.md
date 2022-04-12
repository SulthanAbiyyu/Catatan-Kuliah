---
aliases:
---
# Banker's Algorithm
#OS #bankers-algorithm
> 27-03-2022
```toc
```
### Algorithm
**Prerequisite**:
- 2 dari 3 matriks diketahui (Max, Need, Allocation)
- Available matrix

**Step**:
0. $m$ = jumlah resources dan $n$ = jumlah proses
1. Mencari $\text{Need}$ matrix dengan rumus
$$\text{Need}_{nm} = \sum\limits_{n = 0 \ m =0}^{N \ M} \text{Max}_{nm} - \text{Allocation}_{nm}$$
2. Mencari proses $P_i$ yang mana $\text{Need} \leq \text{Available}$, kalo ketemu nanti dimasukin *safe sequence* lalu merupah status `flag` $P_i$ menjadi 1
3. Selain dimasukin safe sequence, nilai $\text{Available}$ diubah menggunakan rumus
$$\text{Available} = \text{Available} + \text{Allocate}$$
4. Kembali ke step 2 sebanyak sampai semua `flag` ditiap proses menjadi 1
5. Jika, $\forall \ i \in \{0,...,I\}; \ flag_{i} = 1$, maka sistem berada pada safe state. Vice versa.