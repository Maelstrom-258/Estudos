## Soma dos números ímpares
Considere uma **lista da soma dos primeiros n números ímpares**.

$$
\begin{aligned}
1 &= 1 \\
1 + 3 &= 4 \\
1 + 3 + 5 &= 9 \\
1 + 3 + 5 + 7 &= 16 \\
1 + 3 + 5 + 7 + 9 &= 25 \\
...
\end{aligned}
$$
Não temos nenhuma forma de **garantir** que a soma dos primeiros n números ímpares seja $n^2$ .

Então, como que provaríamos o fato?

Definindo o n-ésimo número ímpar: 

$2n-1$ $1+3+...+(2n-3)+(2n-1)=n^2$
$(1+3+...+(2n+3))+(2n-1)$
$(n-1)^2 + (2n-1)$
$(n^2-2n+1)+(2n-1)$
$n^2$

Chegamos a conclusão de que o teorema é sim verdadeiro para o caso aonde $n = 1$
Se o teorema for verdadeiro para $n-1$, ele também será verdadeiro para $n$ .

Dessa forma, pode-se provar que para qualquer caso $n >= 1$  temos o teorema como verdadeiro.

