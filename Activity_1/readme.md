# Atividade 1
Esta atividade se baseia na resolução de 4 questões passada na aula de física computacional do programa de pós graduação da UFU em 2025

As questões resolvidas estão descritas abaixo

## Exercício 1

Implemente o algoritmo de gradiente descendente para encontrar o mínimo da função $U(x) = x^2 -1$. É um caso bem simples para o qual sabemos a solução exata. Ilustre o algoritimo com um gráfico mostrando a função $U(x)$ e a trajetória da partícula. Use inicialmente uma taxa de aprendizado $\alpha = 0.1$ e uma tolerância $\epsilon = 0.01$. O número máximo de iterações deve ser 1000. A posição inicial da partícula deve ser $x_ {0} = 5$. Depois, varie estes parâmetros para ver como eles afetam a convergência do algoritmo.

## Exercício 2

Repita o exercício 1 para a função $U(x) = x^2 (x-1)(x+1)$. Esta função tem dois mínimos globais. Use $x_ {0} = 2$ e tente ajustar $\alpha$ para tentar fazer o código convergir ora num mínimo, ora no outro. O que acontece? O que você pode concluir sobre a escolha da taxa de aprendizado $\alpha$?

## Exercício 3

Repita o exercício 2, mas agora vamos manipular a altura dos mínimos somando uma reta em $U(x)$, tal que a função agora é $U(x) = x^2 (x-1)(x+1) + x/4$. O que acontece? O que você pode concluir sobre a escolha da taxa de aprendizado $\alpha$?

## Exercício 4

Considere agora uma função bidimensional $U(\vec{r}) = U(x,y) = \sin(x)\cos(y) + 2 (xy)^2/1000$. A função tem multiplos mínimos locais. A vizualiação 3D dos passos neste caso pode ser dificil de interpretar. Então, neste caso, para acompanhar a evolução do algoritmo, faça dois gráficos:

a. Um gráfico de contorno (use `plt.imshow` ou `plt.pcolormesh`) da função $U(x,y)$ e desenhe a trajetória da partícula no gráfico.

b. Faça um gráfico do valor de $U(x_ {n}, r_ {n})$ a cada passo como função das iterações (passos) $n$. No contexto de redes neurais chamaremos estes passos de **epochs**.

Varie a posição inicial $(x_ {0}, y_ {0})$ e a taxa de
