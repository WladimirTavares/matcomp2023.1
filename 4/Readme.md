# Número e

O número $e$ pode ser calculado através da seguinte série: 

$$e = \sum_{n=0}^{\infty} 1/n!$$

Podemos estimar o erro de aproximação para o valor $e$ calculando a diferença entre a aproximação atual e aproximação anterior. Para calcular o erro de aproximação relativo, podemos calcular da seguinte maneira:

$$erro\_relativo = (aproximacao\_atual - aproximacao\_anterior)/aproximacao\_atual$$

| Termo | aproximacao | erro\_relativo|
|-------|--------------|---------------|
|  1    |    1         |               |
|  2    |    2         |  0.5          |
|  3    |  2.5000000000| 0.2000000000  |
|  4    |  2.6666666667| 0.0625000000  |



Quando esse erro de aproximação relativo for menor que um certo $\varepsilon$ podemos aceitar a aproximação atual de $e$.

Sua tarefa é encontrar uma aproximação de $e$ considerando que o erro de aproximação relativo deve ser menor que um valor $\varepsilon$.



**Entrada**

A entrada é composta por um número ponto flutuante com precisão dupla representando $\varepsilon$.

**Saída**

A saída é composta por uma única linha contendo uma  aproximação de $e$ tal que  o erro de aproximação relativo de $e$ seja menor que $\varepsilon$.  Imprima essa aproximação com 15 casas decimais.


**Entrada**
```
0.1
```

**Saída**
```
2.666666666666667
```

**Entrada**
```
0.01
```

**Saída**
```
2.716666666666666
```

**Entrada**
```
0.001
```

**Saída**
```
2.718055555555555
```
