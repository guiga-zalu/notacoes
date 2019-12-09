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

Funções compostas, como ![f(g(x))][f g x], ![f][f] de ![g][g] de ![x][x], ou ![(f\circle g)(x)][f circ g x].

### Composição normal de funções

Dada uma função ![f y][f y] e outra ![g x][g x], ![f][f] composta ![g][g] é uma função nova; tem como entrada ![x][x], e saída uma sub-imagem de ![f][f]:

![form 1](https://render.githubusercontent.com/render/math?math=f, g: D_f, D_g \to I_f, I_g)
![form 2](https://render.githubusercontent.com/render/math?math=f%20%3D%20f(a)%2C%20g%20%3D%20g(b))
![form 3](https://render.githubusercontent.com/render/math?math=f(g)%20%3D%20f%5Ccirc%20g%20%3D%20f(g(b))%20%3D%20f%5Ccirc%20g%5Ccirc%20b%3A%20D_%7Bfgb%7D%5Cto%20I_%7Bfgb%7D)
![form 4](https://render.githubusercontent.com/render/math?math=D_%7Bfgb%7D%20%3D%20%7Bb%5Cin%20D_g%3A%20g(b)%20%3D%20g%5Ccirc%20b%5Cin%20D_f%7D)
![form 5](https://render.githubusercontent.com/render/math?math=I_%7Bfgb%7D%20%3D%20%7Bf(g)%5Cin%20I_f%3A%20g%5Cin%20I_g%7D)

### Composição de n-uplas

] ![f][f] uma função da forma ![f = w(x, y, z)](https://render.githubusercontent.com/render/math?math=f%20%3D%20w(x%2C%20y%2C%20z)): 
Seria interessante escrever ![f = w\circle(x, y, z)](https://render.githubusercontent.com/render/math?math=f%20%3D%20w%5Ccircle(x%2C%20y%2C%20z)). 
Ainda, se ![x = x(a), y = y(a), z = z(a)](https://render.githubusercontent.com/render/math?math=x%20%3D%20x(a)%2C%20y%20%3D%20y(a)%2C%20z%20%3D%20z(a)), teremos ![f = w(x, y, z) = w(x(a), y(a), z(a))](https://render.githubusercontent.com/render/math?math=f%20%3D%20w(x%2C%20y%2C%20z)%20%3D%20w(x(a)%2C%20y(a)%2C%20z(a))).


![\] u = (x, y, z):](https://render.githubusercontent.com/render/math?math=%5D%20u%20%3D%20(x%2C%20y%2C%20z)%3A)
![u = (x(a), y(a), z(a))](https://render.githubusercontent.com/render/math?math=u%20%3D%20(x(a)%2C%20y(a)%2C%20z(a)))
![f = w(u) = w(u(a)) = w\circle u\circle a](https://render.githubusercontent.com/render/math?math=f%20%3D%20w(u)%20%3D%20w(u(a))%20%3D%20w%5Ccircle%20u%5Ccircle%20a)
![\therefore f = w\circle(x, y, z)\circle a](https://render.githubusercontent.com/render/math?math=%5Ctherefore%20f%20%3D%20w%5Ccircle(x%2C%20y%2C%20z)%5Ccircle%20a)

Nesta forma, temos que: dada uma n-upla n-dimensional (de comprimento n) de funções, chamada de ![vec x = x_i][vec x = x_i]. 
Temos que:

```latex
\vec{x}(a) = \vec{x}\circle a\\
= (x_1, x_2, ... x_n)\circle a\\
= (x_1(a), x_2(a), ... x_n(a))
```

Nota-se que ![a][a] não é, necessariamente, escalar, podendo ser outra n-upla. 
Assim, podemos ter como definição da notação de composição de n-uplas que: dada uma n-upla de funções ```x = (x_1, x_2, ... x_n)```, ![x][x] composto um argumento (ou lista de argumentos) ![a][a] é igual à n-upla resultado da n-upla de funções ![x_i][x_i] após receber a mesma entrada ![a][a].

### Re-composição de funções

Iniciando por um exemplo, com "seno de seno de x": ```\sin \sin x = \sin(\sin(x)) = (\sin\circ\sin)(x)``` poderia ser representado de forma extremamente simplificada por ```(\sin\circ 2)(x)```, ou "seno composto 2 de x". 
A notação poderia ainda, evoluir para algo mais simples como: ```\sin\circ^2 (x)```, como se o símbolo de composição estivesse sendo elevado ao quadrado. Tomando mais distante notação, algo que em _LaTeX_ um dia poderia ser ```\sin\circ{2}(x)```, com o número 2 acima do símbolo de composição.

Regras:

1. ![f c 2][f c 2]
2. ```f\circ^n = f\circ (f\circ^{n-1}) = f(f\circ^{n-1})```

Nota-se que até a definição atual, [n nat-0][n nat-0].

### Composição Zero

Atravez de outro exemplo, com "seno de x": ```\sin(x) = \sin\circ^1 (x)```. Mas pela regra 2, ```\sin\circ^1 (x) = \sin(\sin\circ^{1-1}(x)) = \sin(\sin\circ^0 (x))```. Extraímos ```\sin\circ^0 (x) = x```. 
Mas como pode haver uma função que, dada uma entrada, tenha como sáida a mesma coisa? 
Na matemática, isso fica a cargo da função identidade ```i(x) = x```. 
Assim, compreende-se que ```\sin\circ^0 (x) = i(x), \sin\circ^0 = i```, ou ainda: ```] f``` uma função, ```f\circ^0 = i```, a função identidade. 
Lê-se: "f composto 0 é igual a identidade".

Regras:

3. ![f c 0][f c 0], a função identidade.

Pela nova definição, ![n nat][n nat].

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

3. ```f\circ(f\circ^{-1}) = (f\circ^{-1})\circ f = f\circ^0 = i```

Ou ainda:

3. ```(f\circ^n)\circ(f\circ^{-n}) = (f\circ^{-n})\circ(f\circ^n) = i```

Temos agora, uma extensão da definição original, agora com ![n int][n int].

Pedido do autor: seria muito interessante uma extensão da definição, que abranja ![n rac][n rac], ![R][R] ou ainda ![C][C].

### Composição Relativa

Tomemos as funções ```exp(x) = e^x``` e ```\ln = exp\circ^{-1}```: ```\circ^{-1}``` refere-se a reversão da função, mas em relação à que? 
Como ```f\circ^0 = i```, temos que a reversão é em relação à ```i```, a função identidade. Assim, podemos escrever ```f\circ^n = f\circ^n_i```, ou ainda num futuro  quando _LaTeX_ abranger a notação, ```f\circ[i]{n}```, com n acima do símbolo de composição e a função referente abaixo. 
Disse "função referente" pois isto abre espaço para a definição de outras funções como referência de inversão e recomposição, como retas (a ex. ```u = -i```) ou ainda curvas das mais variadas.

Pode-se também chegar a uma conclusão de que

Regras:

4. ```f\circ^0_u = u```

### Casos Notáveis

```latex
exp(x) = e^x, \ln = \exp\circ^{-1}\\
(f\circ^{-1})^{(1)} = {1\over f^{(1)}}\\
{df\circ^{-1}\over dx} = {1\over df \ dx} = {dx\over df}\\
u = -i: u\circ^{-1} = u: (-i)\circ^{-1} = -i
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

Imagens em LaTeX vindas de ![LaTeX](https://alexanderrodin.com/github-latex-markdown/)

[f]: https://render.githubusercontent.com/render/math?math=f
[g]: https://render.githubusercontent.com/render/math?math=g
[x]: https://render.githubusercontent.com/render/math?math=x
[x_i]: https://render.githubusercontent.com/render/math?math=x_i
[a]: https://render.githubusercontent.com/render/math?math=a
[f g x]: https://render.githubusercontent.com/render/math?math=f(g(x))
[f circ g x]: https://render.githubusercontent.com/render/math?math=(f%5Ccircle%20g)(x)
[f y]: https://render.githubusercontent.com/render/math?math=f(y)
[g x]: https://render.githubusercontent.com/render/math?math=g(x)
[f c 0]: https://render.githubusercontent.com/render/math?math=f%5Ccircle%5E0%20%3D%20i
[f c 2]: https://render.githubusercontent.com/render/math?math=f(f)%20%3D%20f%5Ccircle%20f%20%3D%20f%5Ccircle%5E2
[n nat]: https://render.githubusercontent.com/render/math?math=n%5Cin%5Cmathbb%7BN%7D
[n nat-0]: https://render.githubusercontent.com/render/math?math=n%5Cin%5Cmathbb%7BN%7D_*
[n int]: https://render.githubusercontent.com/render/math?math=n%5Cin%5Cmathbb%7BZ%7D
[n rac]: https://render.githubusercontent.com/render/math?math=n%5Cin%5Cmathbb%7BQ%7D
[R]: https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BR%7D
[C]: https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BC%7D
[vec x = x_i]: https://render.githubusercontent.com/render/math?math=%5Cvec%7Bx%7D%20%3D%20(x_1%2C%20x_2%2C%20...%20x_n)
