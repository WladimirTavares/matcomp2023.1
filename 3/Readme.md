# Representando números decimais como frações

O número decimal $(0.375)_{10}$ pode ser representado no sistema em ponto flutuante $F(2, 5, -2, 2)$ como $0.11 \times 2^{-1}$, ou seja, $(1/2 + 1/4) \times 2^{-1} = (1/4 + 1/8) = 3/8$. Neste caso, o erro absoluto da representação é 0.

Já o número $(0.1)_{10}$ pode ser representado no sistema ponto flutuante $F(2,5,-5,5)$ como $(0.11001) \times 2^{-3}$ que pode ser representado como fração da seguinte maneira



|$(1/2+1/4+1/32) \times 2^{-3}$| = | $(1/16+1/32+1/256)$|
|-----------------------------|---|-------------|
|                             | = |$(16+8+1)/256$|
|                             | = | $25/256$|


Note que o erro absoluto dessa representação é $1/10 - 25/256 = 6/2560 = 3/1280$






**Entrada**

A entrada é composta por duas linhas. A primeira linha contém uma fração decimal. A segunda linha é composta por 4 números inteiros representando a base $\beta$, a precisão $p$ e os limitantes do expoente $m$ e $M$.

**Saída**

A saída é composta por duas linhas. A primeira linha é composta por uma fração relacionada com representação da fração decimal no sistema em ponto flutuante $F(\beta,p, m, M)$. A segunda linha é composta por uma fração relacionada com o erro absoluto da representação no sistema em ponto flutuante $F(\beta,p, m, M)$.

**Restrições:**

* $M \geq 0$
* $m \leq 0$
* $\beta > 0$
* $p \geq 0$
* $x < 0$


**Entrada**
```
0.1
2 5 -5 5
``` 

**Saída**
```
25/256
3/1280
```

**Entrada**
```
0.01 
2 5 -5 5
``` 

**Saída**
```
underflow
```

**Entrada**
```
0.01
2 5 -6 6
``` 

**Saída**
```
5/512
3/12800
```


**Entrada**
```
0.01
2 10 -6 6
``` 

**Saída**
```
655/65536
9/1638400
```


