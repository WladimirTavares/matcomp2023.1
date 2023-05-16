## Soma MOP

Se nos são apresentados os primeiros $k$ termos de uma sequência, é impossível dizer com certeza o valor do próximo termo, pois existem infinitamente muitas funções polinomiais que podem modelar a sequência.

Como exemplo, vamos considerar a seqüência de números de cubo. Isso é definido pela função geradora,


$$n^3: (1, 8, 27, 64, 125, 216, ...)$$

 

Suponha que só recebêssemos os dois primeiros termos dessa sequência. Trabalhando no princípio de que "simples é melhor", devemos assumir um relacionamento linear e prever que o próximo elemento seja 15 (8-1 = 7 = 15- 8). Mesmo se nos apresentassem os três primeiros termos, pelo mesmo princípio de simplicidade, um relacionamento quadrático deveria ser assumido.

Definiremos $OP (k, n)$ como o n-ésimo termo da função geradora polinomial ótima para os primeiros $k$ termos de uma sequência. Deve ficar claro que $OP (k, n)$ irá gerar com precisão os termos da sequência para $n ≤ k$, e potencialmente o primeiro termo incorreto será $OP (k, k + 1)$; em qual caso nós chamaremos isto de um MOP (Mal OP).


Como base, se nos fosse dado apenas o primeiro termo de seqüência, seria mais sensato assumir constância; isto é, para $n ≥ 2$, $OP (1, n) = a_0$.



Assim, obtemos os seguintes OPs para a seqüência cúbica:



$OP (1, n) = 1 : \quad (1, \textbf{1}, 1, 1, ...)$ 

$OP (2, n) = 7n -6 : \quad (1, 8, \textbf{15}, ...)$

$OP (3, n) = 6n^2-11n + 6 : \quad ( 1, 8, 27, \textbf{58}, ...)$

$OP (4, n) = n^3 : \quad (1, 8, 27, 64, 125, ...)$ 





Claramente, não existem MOPs para k ≥ 4.



Considerando a soma dos MOPs, obtemos 1 + 15 + 58 = 74.



Encontre a soma MOPs para um função geradora de uma sequência.





**Entrada**

A entrada possui duas linhas. A primeira linha contém um inteiro D representando o grau do polinômio dado. A segunda linha N+1 inteiros representando  $a_D,a_{D-1},\ldots,a_0$  representando os coeficientes do grau do polinômio dado tal que  

$$P(n) = a_0 + a_1n+a_2n^2 + \ldots + a_Dn^D$$ 





**Saída**
Devolve um inteiro representando a soma dos MOPS obtidas pelos polinômios   $OP(1,N) + OP(2,N) + \ldots + OP(D-1,N)$ 



**Entrada**
```
3
1 0 0 0
```

**Saída** 
```
74
``` 


**Entrada**
```
4
1 -1 1 -1 1
```

**Saída**
```
670
```


