# Representação de números decimais

Um sistema em ponto flutuante é definido por uma base $\beta$, por uma precisão $p$ e por limitantes $m$ e $M$ para o valor do expoente. Para indicar um determinado sistema em ponto flutuante, escrevemos:

$$F(\beta, p, m, M)$$

Um número qualquer representado nesse sistema F é escrito da seguinte forma:

$$x = \pm 0.d_1d_2\ldots d_p \times \beta^e$$

onde o expoente $e$ é um inteiro tal que $m \leq e \leq M$ e $d_1 \neq 0$, pois a representação deve estar sempre normalizada e $d_1,d_2, \ldots, d_p \in \{0,1,\ldots, \beta-1\}$

Uma fração decimal (chamada simplesmente de números decimais em alguns contextos) é número racional que pode ser representado com frações cujo denominadores são potências de 10. Por exemplo, os decimais 0.8 e 14.89 representam as frações $8/10$ e $1489/100$.

Esses números decimais podem ser representados como aproximações em sistemas em ponto flutuante com a base diferente da base 10.

O processo de conversão de um número decimal para um número ponto flutuante na base $\beta$ pode ser realizado da seguinte maneira. Multiplique o número $x$ pela base $\beta$. Em seguida, calcule a parte inteira de $\beta*x$ e a parte fracionária de $\beta*x$. Observe que se $\beta*x \geq 1$ então $x \geq 1/\beta$. Logo, se a parte inteira de $\beta*x$ representa o primeiro dígito do número ponto flutuante $x$ na base $\beta$. Em seguida, $x$ recebe o valor da parte fracionária de $\beta*x$. 

Considere que você queira representar número decimal 0.375 em um sistema em ponto flutuante com a base 2. 

| x | 2*x | integerPart(2*x) | FractionalPart(2*x) |
|---|-----|----------------|-------------------|
| 0.375 | 0.75 | 0 | 0.75|

O primeiro dígito de $x$ no sistema em ponto flutuante é 0.


Continuando o processo:

| x | 2*x | integerPart(x) | FractionalPart(x) |
|---|-----|----------------|-------------------|
| 0.375 | 0.75 | 0 | 0.75|
| 0.75 | 1.5 | 1 | 0.5|

O segundo dígito de $x$ no sistema em ponto flutuante é 1.

Continuando o processo:

| x | 2*x | integerPart(x) | FractionalPart(x) |
|---|-----|----------------|-------------------|
| 0.375 | 0.75 | 0 | 0.75|
| 0.75 | 1.5 | 1 | 0.5|
| 0.5 | 1.0 | 1 | 0.0|

O terceiro dígito de $x$ no sistema em ponto flutuante é 1.

Logo, o número $(0.375)_{10}$ é representado como $(0.011)_2$. Como o primeiro dígito do sistema em ponto flutuante não pode ser zero, então $(0.011)_2 = 0.11 \times 2^{-1}$.

Observe que esse processo pode continuar indefinidamente. Neste caso, podemos interromper o processo considerando a precisão do nosso sistema em ponto flutuante. 

Sua tarefa é dado um número decimal $x$ e um sistema em ponto fluatuante $F(\beta, p, m, M)$, encontre a representação de $x$ no sistema $F$.


**Entrada**

A entrada é composta por duas linhas. A primeira linha contém uma fração decimal. A segunda linha é composta por 4 números inteiros representando a base $\beta$, a precisão $p$ e os limitantes do expoente $m$ e $M$.

**Saída**

A saída é composta por uma string representando os dígitos do sistema em ponto flutuante e um inteiro representando o expoente no sistema em ponto flutuante.

**Restrições:**

* $M \geq 0$
* $m \leq 0$
* $\beta > 0$
* $p \geq 0$
* $x < 0$


**Entrada**
```
0.1
2 10 -5 5
``` 

**Saída**
```
0.1100110011 -3
```

**Entrada**
```
0.2 
2 10 -5 5
``` 

**Saída**
```
0.1100110011 -2
```




