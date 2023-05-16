# Brincadeira do Augusto

Augusto gosta muito da seguinte brincadeira: dada a sequência 1, 2, 3, 4, 5, qual é a próximo número? Às vezes é muito fácil responder, às vezes pode ser bem difícil. Augusto notou que essas perguntas podem ser resolvidas descrevendo a sequência usando polinômios. Por exemplo, a seqüência 1, 2, 3, 4, 5 pode ser facilmente entendida como um polinômio trivial,  $P(n)=n$ . O próximo número será 6. Mas sequências ainda mais complexas, como 1, 2, 4, 7, 11, podem ser descritas por um polinômio. Neste caso,  o polinômio que descreve esta sequência é  $\frac{1}{2}n^2 - \frac{1}{2}n+1$ . Note que mesmo se os membros da sequência são inteiros, os coeficientes polinomiais podem ser quaisquer números reais.

Um polinômio é uma expressão da seguinte forma:

  $P(n) = a_Dx^D + a_{D-1}n^{D-1} + \ldots + a_1n + a_0$

 

Se  $a_D \neq 0$ , o número $D$ é chamado de grau do polinômio. Note que a função constante $P (n) = C$ pode ser considerado como polinômio de grau 0.

Sua tarefa é dada uma sequência com comprimento N encontre o menor grau de um polinômio que pode ser usado para descrever uma sequência.



**Entrada**

A entrada do problema é composta por duas linhas. A primeira linha possui um inteiro N representando o comprimento da sequência dada. 

A segunda linha contém N números inteiros $x_0,x_1,..,x_{n-1}$ separados por um espaço. Esses números forma a sequência dada. 

**Saída**

Imprima um inteiro D representando o menor grau possível de um polinômio P(n) tal que $P(i) = x_i$, para todo $i = 0, .., n-1$.

**Entrada**
```
5
1 2 3 4 5
```
**Saída**
```
1
```
**Entrada**
```
5
1 2 4 7 11
```
**Saída**
```
2
```