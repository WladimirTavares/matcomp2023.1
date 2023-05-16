## Método de Simpson 1/3

O método de Simpson 1/3 consiste em aproximar a função  f(x)  no intervalo  $[x_{i-1}, x_{i+1}]$  pelo polinômio interpolador de grau 2 que passa pelos pontos  $(x_{i-1}, f(x_{i-1})), (x_i, f(x_i))   e  (x_{i+1}, f(x_{i+1}))$ .

<div>
<center>
    <img src="https://drive.google.com/uc?export=view&id=1pVqYgog9728GTlYGprU4YdZxd3Qbx9ih" width="400"/>
</center>
</div>

Usando o polinômio interpolador de grau 2, obtemos a  seguinte aproximação

$$\int_{x_{i-1}}^{x_{i+1}} f(x) dx = \frac{h}{3}[ f_{i-1} + 4f_i + f_{i+1}]$$

 

onde  $$h = (x_{i+1} - x_{i-1})/2 $$



A regra de simpson composta consiste em dividir o intervalo em N subintervalos e aplicar a regra de simpson em cada subintervalo.

Dado um função polinomial $f(x)$, sua tarefa é calcular a integral $f(x)$ no intervalo $[A,B]$ usando a regra de simpson composta realizando a divisão em N intervalos.

**Entrada**

A entrada possui três linhas. A primeira linha contém um inteiro $D$ representando o grau do polinômio dado.

A segunda linha possui $D+1$ inteiros  $a_0, \ldots , a_{D}$  representando os coeficientes do polinômio dado tal que 

$$P(x) = a_0 + a_1 x + a_2 x^2 + \ldots + a_D x^D$$ 

A terceira linha possui três inteiros $A$, $B$ e $N$ sendo que $[A,B]$ representa o intervalo de integração e N representa a quantidade de subintervalos da regra de simpson composta.



Saída

Imprima um número ponto flutuante com cinco casas decimais depois da vírgula representando o valor aproximado da integral calculada usando a regra de simpson composta.



**Entrada**
```
4
3 2 1 2 1
0 1 1
```

**Saída**
```
5.04167
```


**Entrada**
```
4
3 2 1 2 1
0 1 2
```

**Saída**
```
5.03385
```
