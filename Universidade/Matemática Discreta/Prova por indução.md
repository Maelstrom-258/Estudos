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

$$\begin{aligned}
2n-1 \\
1+3+...+(2n-3)+(2n-1)=n^2 \\
(1+3+...+(2n+3))+(2n-1) \\
(n-1)^2 + (2n-1) \\
(n^2-2n+1)+(2n-1) \\
n^2
\end{aligned}$$

Chegamos a conclusão de que o teorema é sim verdadeiro para o caso aonde $n = 1$
Se o teorema for verdadeiro para $n-1$, ele também será verdadeiro para $n$ .

Dessa forma, pode-se provar que para qualquer caso $n \geq 1$  temos o teorema como verdadeiro.
## Prova por indução
Temos um **Caso base**, onde que vamos mostrar que o teorema é verdadeiro para o primeiro valor da sequência a ser considerada.
Uma vez demonstrado o caso base, temos o **Passo indutivo**, onde o mesmo tem 3 sub componentes.
1) Hipótese indutiva: O que vai ser assumido como verdadeiro (que o teorema é válido para um dado valor $n$.
2) Tese: O que quer ser provado, demonstrado, ou validado. (Se o teorema for válido para o falor da sequência, ele será para o próximo valor após ele)
3) Demonstração: Partindo da hipótese, mostrar que a tese tem que ser verdadeira no caso da hipótese indutiva, validando a tese.


