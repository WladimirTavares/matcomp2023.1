## Dieta do Gabriel

Gabriel realiza atividade físicas moderada sempre a uma temperatura ambiente. Como ele não quer realizar atividades físicas mais intensa, ele quer mudar a sua dieta.

Gabriel encontrou a tabela abaixo relaciona a quantidade ideal de calorias em função da idade e do peso para homens que realizam atividade física moderada a uma temperatura ambiente.

<div>
<center>
    <img src="https://drive.google.com/uc?export=view&id=1JMH3EJIh4-E6Rcj1rvPOcA87DJuQIpoe" width="350"/>
</center>
</div>


Agora, Gabriel precisa de sua ajuda usando uma interpolação quadrática dupla, ele precisa determinar a cota aproximada de calorias para um homem de N anos que pesa M kg.


**Entrada**

A entrada possui dois inteiros N ( 25 <= N <= 65 )e  M ( 50 <= M <= 70) separados por um espaço.

**Saída**

Imprima um número ponto flutuante com 5 casas decimais depois da vírgula representando a cota aproximada de calorias para um homem de N anos que pesa M kg. 

**Entrada**

30 55

**Saída**

2670.11719



Instruções: Aparentemente, a ordem das interpolações pode afetar o valor do resultado. Os resultados foram calculados encontrando primeiro a cota aproximada de calorias para um homem com peso M e depois foi calculado para a idade N.