# Reações Químicas Reversíveis

As reações químicas reversíveis são aquelas que podem ocorrer tanto no sentido direto como no sentido inverso, ou seja, pode ser revertidas.

Por exemplo,

$$2A + B \leftrightarrow C$$

pode ser caracterizada pela seguinte relação de equilíbrio:

$$K = \frac{c_c}{c_a^2 c_b}$$

$c_i$  representa a concentração do elemento químico $i$.

Vamos definir uma variável $x$ representando o número de mols de $C$ produzidos. A conservação de massa pode ser usada para reformular a relação de equilíbrio como

$$K = \frac{c_{c,0} + x}{(c_{a,0} - 2x)^2(c_{b,0} - x)}$$

onde o subscrito 0 representa a concetração inicial de cada elemento.

Dado o valor de $K$, $c_{a,0}$,$c_{b,0}$, $c_{c,0}$ determine o valor de $x$ considerando o chute inicial de $x_l$ e $x_u$ e com $n$ algarismos significativos, ou seja, um intervalo (a,b) possui uma solução aproximada se $|b-a|$ é menor que $0.5 \times 10^{-n}$


**Entrada**

A entrada é composta por um linha com 7 valores $K$, $c_{a,0}$,$c_{b,0}$, $c_{c,0}$,$x_l$, $x_u$ e $\varepsilon$ representando constante de equílibrio, concetração inicial dos elementos A, B, C, intervalo inicial e final para o número de mols produzidos de $C$ e o limite do erro aceito.



**Saída**

A saída é composta de uma única linha contendo o número de mols produzidos de C com n casas decimais. A solução deve ser truncada para n casas decimais.

Utilize a seguinte função:

```python
def truncate(f, n):
    '''Truncates/pads a float f to n decimal places without rounding'''
    s = '%.12f' % f
    i, p, d = s.partition('.')
    return '.'.join([i, (d+'0'*n)[:n]])
```


**Entrada**
```
0.016 42 28 4 0 20 2
```

**Saída**
```
15.92
```

**Entrada**
```
0.012 42 28 4 0 20 2
```

**Saída**
```
15.35
```