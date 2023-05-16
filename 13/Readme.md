## Problema do comprimento de um arco

Nós queremos determinar o comprimento de uma função $y = f(x)$ em um intervalo $[a,b]$. 

Inicialmente, vamos estimar o comprimento da curva, dividindo o intervalo em $n$ subintervalos cada com largura $\Delta x$ e vamos denotar o ponto na curva em cada ponto por $P_i$. Podemos então aproximar a curva por uma série de linhas retas conectando os pontos.

<div>
<center>
    <img src="https://drive.google.com/uc?export=view&id=1Hq2M9r7tp9y6NfhtaAP8pWiqZMe_7H0t" width="400"/>
</center>
</div>

Agora podemos denotar o comprimento de cada um dos segementos de linhas pela distâncias entre os pontos $P_{i-1}$ e $P_i$. Logo, o comprimento $L$ da curva será:

$$L = \sum_{i=1}^{n} dist(P_{i-1}, P_i)$$

Em cada segmento, vamos definir $\Delta y_i = y_i - y_{i-1} = f(x_i) - f(x_{i-1})$. O comprimento de cada segmento será:

$$dist(P_{i-1}, P(i)) = \sqrt{(x_i - x_{i-1})^2 +  (y_i - y_{i-1})^2} = \sqrt{ \Delta x_i^2 + \Delta y_i^2}$$

Pelo Teorema do Valor Médio, sabemos que existe um ponto $x_i^* \in [x_{i-1},_i]$ tal que

$$
\begin{align*}
f(x_i) - f(x_{i-1}) & = & f'(x_i^*)(x_i - x_{i-1})\\
\Delta y_i & = & f'(x_i^*) \Delta x
\end{align*}
$$

Portanto, o comprimento da curva será escrito como:

$$
\begin{align*}
dist(P_{i-1},P_i) & = & \sqrt{(x_i - x_{i-1})^2 +  (y_i - y_{i-1})^2}\\
& = & \sqrt{(\Delta x)^2 +  (\Delta y_i)^2}\\
& = & \sqrt{\Delta x^2 +  f'(x_i*) \Delta x^2}\\
& = & \sqrt{\Delta x^2 [ 1 +  f'(x_i*)] }\\
& = & \Delta x \sqrt{ [ 1 +  f'(x_i*)] }\\
\end{align*}
$$

O comprimento exato da curva será:

$$
\begin{align*}
L  & = & \lim_{n \gets \infty} \sum_{i=1}^{n} dist(P_{i-1},P_i)\\
& = & \lim_{n \gets \infty} \sum_{i=1}^{n} \Delta x\sqrt{1 + f'(x_i)}\\
\end{align*}
$$

Usando a definição de integral:

$$L = \int_{a}^{b} \sqrt{1 + f'(x_i)} dx$$

Por exemplo, seja $f(x) = x^2$. Calcule o comprimento do arco da função $f(x)$ no intervalo entre $(1,3)$

A função $f'(x) = 2x$, então $[f'(x)]^2 = 4x^2$. Portanto, o comprimento do arco será:

$$L = \int_{1}^{3} \sqrt{1 + 4x^2} \approx 8.26815$$


**Entrada**

A entrada possui três linhas. A primeira linha contém um inteiro $n$ representando o grau do polinômio dado. A segunda linha $n+1$ inteiros representando  $a_n,a_{n-1},\ldots,a_0$  representando os coeficientes do grau do polinômio dado tal que  

$$P(x) = a_nx^n + a_{n-1}x^{n-1}+ \ldots + a_1x + a_0$$ 

A terceira linha contém dois inteiros a e b representando os limites do intervalo.

Utilize como tolerância $0.000001$.

**Saída**

Devolva um número ponto com 5 casas decimais representando o comprimento da curva $f(x)$ no intervalo entre $[a,b]$


**Entrada**
```
2
1 0 0
1 3
```

**Saída** 
```
8.26815
``` 

**Entrada**
```
2
1 2 3
```

**Saída** 
```
12.17185
``` 

