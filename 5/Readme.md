# Critério das Linhas 

Os métodos iterativos para resolução de sistemas lineares produzem menos erros de arrendondamento e tem a garantia da convergência se as condições de convergência são asseguradas.

No método de Gauss-Jacobi, temos o seguinte critério de convergência:

Dado um sistema linear $Ax = b$. Seja 

$$\alpha_i = (\sum_{ 1 \leq j \leq n, j \neq i} |a_{ij}|)/|a_{ii}|$$

e

$$\alpha = \max_{ 1 \leq i \leq n} \alpha_i$$


Se $\alpha < 1$ então o método de Gauss-Jacobi gera uma sequência convergente para a solução de um sistema dado, independentemente da escolha da aproximação inicial.

Cheque se um sistema linear satisfaz o critério das linhas considerando a permutação de linhas e colunas. 

Por exemplo, a matriz
$$
A = \begin{bmatrix}
10 & 2 & 1\\
2 & 3 & 10\\
1 & 5 & 1\\
\end{bmatrix}
$$

não satisfaz o critério da linhas na linha 2. Contudo se trocarmos a coluna 2 e 3, obtemos a seguinte matriz:

$$
A = \begin{bmatrix}
10 & 1  & 2\\
2 & 10  & 3\\
1 & 1  & 5\\
\end{bmatrix}
$$

que satisfaz o critério das linhas.

Dado uma matriz A, mostre se é possível realizar trocas de linhas e colunas de maneira que o critério das linhas seja satisfeita.

**Entrada**

A entrada é composta por um número um inteiro $n$. As $n$ linhas seguintes possuem $n$  inteiros representando os coeficientes de uma matriz $A$.



**Saída**

A entrada é composta por uma linha contendo a palavra `yes` se a matriz A satisfaz o critério das linhas e `no` se a matriz não satifaz o critério das linhas.

**Entrada**
```
3
10 2 1
1 5 1
2 3 10
```

**Saída**
```
yes
```

**Entrada**
```
3
1 3 1
5 2 2
0 6 8
```

**Saída**
```
yes
```

**Entrada**
```
2
1 1 
1 -3
```

**Saída**
```
no
```
