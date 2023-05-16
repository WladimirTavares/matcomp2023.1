# Sistema em Ponto Flutuante

Um sistema em ponto flutuante é definido por uma base $\beta$, por uma precisão $p$ e por limitantes $m$ e $M$ para o valor do expoente. Para indicar um determinado sistema em ponto flutuante, escrevemos:

$$F(\beta, p, m, M)$$

Um número qualquer representado nesse sistema F é escrito da seguinte forma:

$$x = \pm 0.d_1d_2\ldots d_p \times \beta^e$$

onde o expoente $e$ é um inteiro tal que $m \leq e \leq M$ e $d_1 \neq 0$, pois a representação deve estar sempre normalizada e $d_1,d_2, \ldots, d_p \in \{0,1,\ldots, \beta-1\}$

Sua tarefa é dado um sistema em ponto flutuante devolva o menor e o maior número representado nesse sistema F como uma fração.

**Entrada**

A entrada é composta por 4 números inteiros representando a base $\beta$, a precisão $p$ e os limitantes do expoente $m$ e $M$.

**Saída**

A saída é composta por dois números inteiros representando o númerador e o denominador do maior e do menor número representado no sistema em ponto flutuante.

**Restrições:**

* $M \geq 0$
* $m \leq 0$
* $\beta > 0$
* $p \geq 0$


**Entrada**
```
10 4 -3 3
``` 

**Saída**
```bash
9999/10
1/10000
```

**Entrada**
```
2 3 -3 3
``` 

**Saída**
```
7/1
1/16
```




