# Notações Especiais

Autor: [Guilherme Alves Ceobaniuk Zaluchi](https://guilherme.zaluchi.com.br) <[guilherme@zaluchi.com.br](mailto:guilherme@zaluchi.com.br)>

Lista de notações matemáticas utilizadas em meus trabalhos.

## Índice

1. Composição de funções
   1. Composição normal de funções
   2. Composição de n-uplas
   3. Composição Zero
   4. Re-composição de funções
   5. Reversão de funções
   6. Composição relativa
   7. Casos Notáveis
2. Contagem
   1. Contagem de Conjunto
   2. Contagem de n-upla
   3. Log de conjunto
3. Derivadas
   1. Diretas
      1. Interpretação algébrica
      2. Interpretação real
   2. Direcionais
4. Vetores numéricos
   1. Índice de um vetor numérico
   2. Moda de um vetor numérico
   3. Vetor numérico _n

## Composição de funções

Funções compostas, como ```latex f(g(x))```, ```latex f``` de ```latex g``` de ```latex x```, ou ```latex (f\circle g)(x)```.

### Composição normal de funções

Dada uma função ```latex f(y)``` e outra ```latex g(x)```, ```latex f``` composta ```latex g``` é uma função nova; tem como entrada ```latex x```, e saída uma sub-imagem de ```latex f```:

```latex
] f, g: D_f, D_g \to I_f, I_g\\
f = f(a), g = g(b)\\
f(g) = f\circle g = f(g(b)) = f\circle g\cirlce b: D_{fgb}\to I_{fgb}\\
D_{fgb} = {b\in D_g: g(b) = g\circle b\in D_f}\\
I_{fgb} = {f(g)\in I_f: g\in I_g}
```

### Composição de n-uplas

```latex ] f``` uma função da forma ```latex f = w(x, y, z)```: 
Seria interessante escrever ```latex f = w\circle(x, y, z)```. 
Ainda, se ```latex x = x(a), y = y(a), z = z(a)```, teremos ```latex f = w(x, y, z) = w(x(a), y(a), z(a))```.

```latex
] u = (x, y, z):\\
u = (x(a), y(a), z(a))\\
f = w(u) = w(u(a)) = w\circle u\circle a\\
\therefore f = w\circle(x, y, z)\circle a
```

Nesta forma, temos que: dada uma n-upla n-dimensional (de comprimento n) de funções, chamada de ```latex \vec{x} = (x_1, x_2, ... x_n)```. 
Temos que:

```latex
\vec{x}(a) = \vec{x}\circle a\\
= (x_1, x_2, ... x_n)\circle a\\
= (x_1(a), x_2(a), ... x_n(a))
```

Nota-se que ```latex a``` não é, necessariamente, escalar, podendo ser outra n-upla. 
Assim, podemos ter como definição da notação de composição de n-uplas que: dada uma n-upla de funções ```latex x = (x_1, x_2, ... x_n)```, ```latex x``` composto um argumento (ou lista de argumentos) ```latex a``` é igual à n-upla resultado da n-upla de funções ```latex x_i``` após receber a mesma entrada ```latex a```.

### Re-composição de funções

Iniciando por um exemplo, com "seno de seno de x": ```latex \sin \sin x = \sin(\sin(x)) = (\sin\circle\sin)(x)``` poderia ser representado de forma extremamente simplificada por ```latex (\sin\circle 2)(x)```, ou "seno composto 2 de x". 
A notação poderia ainda, evoluir para algo mais simples como: ```latex \sin\circle^2 (x)```, como se o símbolo de composição estivesse sendo elevado ao quadrado. Tomando mais distante notação, algo que em _LaTeX_ um dia poderia ser ```latex \sin\circle{2}(x)```, com o número 2 acima do símbolo de composição.

Regras:

1. ```latex f(f) = f\circle f = f\circle^2```
2. ```latex f\circle^n = f\circle (f\circle^{n-1}) = f(f\circle^{n-1})```

Nota-se que até a definição atual, ```latex n\in\mathbb{N}_*```.

### Composição Zero

Atravez de outro exemplo, com "seno de x": ```latex \sin(x) = \sin\circle^1 (x)```. Mas pela regra 2, ```latex \sin\circle^1 (x) = \sin(\sin\circle^{1-1}(x)) = \sin(\sin\circle^0 (x))```. Extraímos ```latex \sin\circle^0 (x) = x```. 
Mas como pode haver uma função que, dada uma entrada, tenha como sáida a mesma coisa? 
Na matemática, isso fica a cargo da função identidade ```latex i(x) = x```. 
Assim, compreende-se que ```latex \sin\circle^0 (x) = i(x), \sin\circle^0 = i```, ou ainda: ```latex ] f``` uma função, ```latex f\circle^0 = i```, a função identidade. 
Lê-se: "f composto 0 é igual a identidade".

Regras:

3. ```latex f\circle^0 = i```, a função identidade.

Pela nova definição, ```latex n\in\mathbb{N}```.

### Reversão de funções

Mais uma vez, pela regra recursiva, a regra 2, tomemos outro exemplo (com senos): 
```latex i = \sin\circle^0 = \sin(\sin\circle^{0-1}) = \sin(\sin\circle^{-1})```. Obtém-se a informação de que o seno de uma função desconhecida é igual à função identidade. Antes de definir algo em relação à ```latex \sin\circle^{-1}```, coloquemos tudo na função reversa ao seno, arcseno: 
```latex \arcsin(i) = \arcsin(\sin(\sin\circle^{-1})) = \sin\circle^{-1}``` 
Como arcseno é reversa à seno, ```latex \arcsin(\sin) = \sin(\arcsin) = i```. Com esta substituição, extraímos que ```latex \arcsin = \sin\circle^{-1}```. 
Assim, se ```latex f``` é uma função, ```latex f\circle^{-1}``` é a função reversa à ```latex f```. 
Lê-se: "f composta -1 é a função reversa à f".

Com atenção especial as funções trigonométricas, podemos escrever ```latex \sin\circle^{-1}``` ao invés de ```latex \arcsin``` ou ainda, a confusa ```latex \sin^{-1}```.

Reescrevendo a regra da anulação de composição, a regra 3:

Regra:

3. ```latex f\circle(f\circle^{-1}) = (f\circle^{-1})\circle f = f\circle^0 = i```

Ou ainda:

3. ```latex (f\circle^n)\circle(f\circle^{-n}) = (f\circle^{-n})\circle(f\circle^n) = i```

Temos agora, uma extensão da definição original, agora com ```latex n\in\mathbb{Z}```.

Pedido do autor: seria muito interessante uma extensão da definição, que abranja ```latex n\in\mathbb{Q}```, ```latex \mathbb{R}``` ou ainda ```latex \mathbb{C}```.

### Composição Relativa

Tomemos as funções ```latex exp(x) = e^x``` e ```latex \ln = exp\circle^{-1}```: ```latex \circle^{-1}``` refere-se a reversão da função, mas em relação à que? 
Como ```latex f\circle^0 = i```, temos que a reversão é em relação à ```latex i```, a função identidade. Assim, podemos escrever ```latex f\circle^n = f\circle^n_i```, ou ainda num futuro  quando _LaTeX_ abranger a notação, ```latex f\circle[i]{n}```, com n acima do símbolo de composição e a função referente abaixo. 
Disse "função referente" pois isto abre espaço para a definição de outras funções como referência de inversão e recomposição, como retas (a ex. ```latex u = -i```) ou ainda curvas das mais variadas.

Pode-se também chegar a uma conclusão de que

Regras:

4. ```latex f\circle^0_u = u```

### Casos Notáveis

```latex
exp(x) = e^x, \ln = \exp\circle^{-1}\\
(f\circle^{-1})^{(1)} = {1\over f^{(1)}}\\
{df\circle^{-1}\over dx} = {1\over df \ dx} = {dx\over df}\\
u = -i: u\circle^{-1} = u: (-i)\circle^{-1} = -i
```

--------

## Contagem

### Contagem de Conjunto

### Contagem de n-upla

### Log de conjunto

--------

## Derivadas

### Diretas

#### Interpretação algébrica

#### Interpretação real

### Direcionais
