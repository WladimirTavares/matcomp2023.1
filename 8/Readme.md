# Busca Ternária

A busca ternária é um algoritmo de busca que divide o intervalo de busca em três partes iguais e realiza a busca em cada uma dessas partes. É uma variação da busca binária, que divide o intervalo de busca em duas partes iguais.

O funcionamento da busca ternária é simples: primeiro, é verificado se o elemento buscado está no primeiro terço do intervalo de busca. Se estiver, a busca é realizada nesse terço. Caso contrário, é verificado se o elemento está no segundo terço do intervalo. Se estiver, a busca é realizada nesse terço. Por fim, se o elemento não estiver nos dois primeiros terços, é verificado se ele está no terceiro terço do intervalo. Se estiver, a busca é realizada nesse terço.

Dado um intervalo $[l,h]$:

* O primeiro intervalo $[l, l + (h-l)/3]$
* O segundo intervalo $[l + (h-l)/3, l + 2*(h-l)/3]$
* O terceiro intervalo $[l + 2*(h-l)/3, h]$ 

Dado um polinômio de grau $n$, um chute inicial da raiz da equação [l, h] e um tolerância, aplique o algoritmo de busca ternária para encontrar uma raiz da equação.




**Entrada**

A entrada é composta por 4 linhas. A primeira linha contém um inteiro ($2 \leq N \leq 9$) representando o grau do polinômio. A segunda linha contém N+1 números reais. A terceira linha contém dois números reais $l, h$ representando o chute inicial do intervalo da raiz. A quarta linha contém um número real denotando a tolerância utilizada no critério de parada.

**Saída**

A saída é composta por duas linhas. A primeira linha contém a seguinte mensagem:
```
busca ternaria realizou X iteracoes
```

A segunda linha contém a seguinte mensagem:

```
a solucao está no intervalo [a,b]
```

com a e b com 10 casas decimais.

**Entrada**
```
2
-0.6 2.4 5.5
5 10
0.001
```

**Saída**
```
busca ternaria realizou 9 iteracoes
a solucao está no intervalo [5.627953056,5.628715135]
```


**Dica:** 

Modifique o seguinte algoritmo do método da bissecao:
```python
def f(n, a, x):
    ret = 0
    for i in range(n+1):
        ret = ret * x + a[i]
    return ret
    
def binary_search(n, a, l, h, tol):
    iteracao = 1
    while True:
        if abs(h-l) < tol:
            return l, h, iteracao
        m1 = l + (h-l)/2
        if f(n,a,l)*f(n,a,m1) < 0:
            h = m1
        else:
            l = m1 
                 
        iteracao += 1

```