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

Funções compostas, como ```f(g(x))```, ```f``` de ```g``` de ```x```, ou ```(f\circle g)(x)```.

### Composição normal de funções

Dada uma função ```f(y)``` e outra ```g(x)```, ```f``` composta ```g``` é uma função nova; tem como entrada ```x```, e saída uma sub-imagem de ```f```:

```latex
] f, g: D_f, D_g \to I_f, I_g\\
f = f(a), g = g(b)\\
f(g) = f\circle g = f(g(b)) = f\circle g\cirlce b: D_{fgb}\to I_{fgb}\\
D_{fgb} = {b\in D_g: g(b) = g\circle b\in D_f}\\
I_{fgb} = {f(g)\in I_f: g\in I_g}
```

### Composição de n-uplas

```] f``` uma função da forma ```f = w(x, y, z)```: 
Seria interessante escrever ```f = w\circle(x, y, z)```. 
Ainda, se ```x = x(a), y = y(a), z = z(a)```, teremos ```f = w(x, y, z) = w(x(a), y(a), z(a))```.

```latex
] u = (x, y, z):\\
u = (x(a), y(a), z(a))\\
f = w(u) = w(u(a)) = w\circle u\circle a\\
\therefore f = w\circle(x, y, z)\circle a
```

Nesta forma, temos que: dada uma n-upla n-dimensional (de comprimento n) de funções, chamada de ```\vec{x} = (x_1, x_2, ... x_n)```. 
Temos que:

```latex
\vec{x}(a) = \vec{x}\circle a\\
= (x_1, x_2, ... x_n)\circle a\\
= (x_1(a), x_2(a), ... x_n(a))
```

Nota-se que ```a``` não é, necessariamente, escalar, podendo ser outra n-upla. 
Assim, podemos ter como definição da notação de composição de n-uplas que: dada uma n-upla de funções ```x = (x_1, x_2, ... x_n)```, ```x``` composto um argumento (ou lista de argumentos) ```a``` é igual à n-upla resultado da n-upla de funções ```x_i``` após receber a mesma entrada ```a```.

### Re-composição de funções

Iniciando por um exemplo, com "seno de seno de x": ```\sin \sin x = \sin(\sin(x)) = (\sin\circle\sin)(x)``` poderia ser representado de forma extremamente simplificada por ```(\sin\circle 2)(x)```, ou "seno composto 2 de x". 
A notação poderia ainda, evoluir para algo mais simples como: ```\sin\circle^2 (x)```, como se o símbolo de composição estivesse sendo elevado ao quadrado. Tomando mais distante notação, algo que em _LaTeX_ um dia poderia ser ```\sin\circle{2}(x)```, com o número 2 acima do símbolo de composição.

Regras:

1. ```f(f) = f\circle f = f\circle^2```
2. ```f\circle^n = f\circle (f\circle^{n-1}) = f(f\circle^{n-1})```

Nota-se que até a definição atual, ```n\in\mathbb{N}_*```.

### Composição Zero

Atravez de outro exemplo, com "seno de x": ```\sin(x) = \sin\circle^1 (x)```. Mas pela regra 2, ```\sin\circle^1 (x) = \sin(\sin\circle^{1-1}(x)) = \sin(\sin\circle^0 (x))```. Extraímos ```\sin\circle^0 (x) = x```. 
Mas como pode haver uma função que, dada uma entrada, tenha como sáida a mesma coisa? 
Na matemática, isso fica a cargo da função identidade ```i(x) = x```. 
Assim, compreende-se que ```\sin\circle^0 (x) = i(x), \sin\circle^0 = i```, ou ainda: ```] f``` uma função, ```f\circle^0 = i```, a função identidade. 
Lê-se: "f composto 0 é igual a identidade".

Regras:

3. ```f\circle^0 = i```, a função identidade.

Pela nova definição, ```n\in\mathbb{N}```.

### Reversão de funções

Mais uma vez, pela regra recursiva, a regra 2, tomemos outro exemplo (com senos): 
```i = \sin\circle^0 = \sin(\sin\circle^{0-1}) = \sin(\sin\circle^{-1})```. Obtém-se a informação de que o seno de uma função desconhecida é igual à função identidade. Antes de definir algo em relação à ```\sin\circle^{-1}```, coloquemos tudo na função reversa ao seno, arcseno: 
```\arcsin(i) = \arcsin(\sin(\sin\circle^{-1})) = \sin\circle^{-1}``` 
Como arcseno é reversa à seno, ```\arcsin(\sin) = \sin(\arcsin) = i```. Com esta substituição, extraímos que ```\arcsin = \sin\circle^{-1}```. 
Assim, se ```f``` é uma função, ```f\circle^{-1}``` é a função reversa à ```f```. 
Lê-se: "f composta -1 é a função reversa à f".

Com atenção especial as funções trigonométricas, podemos escrever ```\sin\circle^{-1}``` ao invés de ```\arcsin``` ou ainda, a confusa ```\sin^{-1}```.

Reescrevendo a regra da anulação de composição, a regra 3:

Regra:

3. ```f\circle(f\circle^{-1}) = (f\circle^{-1})\circle f = f\circle^0 = i```

Ou ainda:

3. ```(f\circle^n)\circle(f\circle^{-n}) = (f\circle^{-n})\circle(f\circle^n) = i```

Temos agora, uma extensão da definição original, agora com ```n\in\mathbb{Z}```.

Pedido do autor: seria muito interessante uma extensão da definição, que abranja ```n\in\mathbb{Q}```, ```\mathbb{R}``` ou ainda ```\mathbb{C}```.

### Composição Relativa

Tomemos as funções ```exp(x) = e^x``` e ```\ln = exp\circle^{-1}```: ```\circle^{-1}``` refere-se a reversão da função, mas em relação à que? 
Como ```f\circle^0 = i```, temos que a reversão é em relação à ```i```, a função identidade. Assim, podemos escrever ```f\circle^n = f\circle^n_i```, ou ainda num futuro  quando _LaTeX_ abranger a notação, ```f\circle[i]{n}```, com n acima do símbolo de composição e a função referente abaixo. 
Disse "função referente" pois isto abre espaço para a definição de outras funções como referência de inversão e recomposição, como retas (a ex. ```u = -i```) ou ainda curvas das mais variadas.

Pode-se também chegar a uma conclusão de que

Regras:

4. ```f\circle^0_u = u```

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
