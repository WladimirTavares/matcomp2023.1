# Paraquedismo

A velocidade de um paraquedista em queda livre é dado por 

$$v = \frac{gm}{c}(1 - e^{-(c/m)t})$$

onde 

* $g = 9,8m/s^2$
* m representa a massa do paraquedista.
* c representa coeficiente de arrasto
* t representa o tempo

Um paraquedista deseja atingir uma velocidade máxima de $V$ m/s em seu salto de paraquedas. Determine a massa mínima do seu corpo, considerando que ele está usando um paraquedas com um coeficiente de arrasto de $c$ Kg/s e que ele deseja atingir a velocidade máxima $V$ em $t$ segundos após a abertura do paraquedas. Considere que a massa do paraquedista está entre 50 e 100 kg. Resolva com o método da bisseção considerando como critério de parada quando o intervalo da solução for menor 0.001.


**Entrada**

A entrada é composta por quatro números $c$, $V$ e $t$  representando o coeficiente de arrasto, a velocidade máxima que o paraquedista deseja atingir e o tempo após a abertura do paraquedas.

**Saída**

A saída é composta de uma única linha contendo a massa mínima do paraquedista com 2 casas decimais. 


**Entrada**
```
15 35 9
```

**Saída**
```
59.84
```

**Entrada**
```
20 35 9 
```

**Saída**
```
79.79
```