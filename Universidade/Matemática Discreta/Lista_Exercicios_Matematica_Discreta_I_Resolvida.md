# 1ª Lista de Exercícios de Matemática Discreta I

**Universidade Federal Rural de Pernambuco (UFRPE)**  
**Departamento de Computação (DC)**

---

## 1. Oposta, contrapositiva e inversa

Para uma proposição condicional:

$$
p \rightarrow q
$$

temos:

- **Oposta:** $p \land \neg q$
- **Contrapositiva:** $\neg q \rightarrow \neg p$
- **Inversa:** $\neg p \rightarrow \neg q$

### a) Se nevar esta noite, então ficarei em casa

Defina:

- $p$: nevar esta noite
- $q$: ficarei em casa

**Oposta:**

> Neva esta noite e eu não fico em casa.

**Contrapositiva:**

> Se eu não ficar em casa, então não nevará esta noite.

**Inversa:**

> Se não nevar esta noite, então não ficarei em casa.

### b) Eu vou à praia sempre que faz um dia ensolarado de verão

Defina:

- $p$: vou à praia
- $q$: faz um dia ensolarado de verão

"Eu vou à praia sempre que faz um dia ensolarado de verão" corresponde a:

$$
q \rightarrow p
$$

**Oposta:**

> Faz um dia ensolarado de verão e eu não vou à praia.

**Contrapositiva:**

> Se eu não vou à praia, então não faz um dia ensolarado de verão.

**Inversa:**

> Se não faz um dia ensolarado de verão, então eu não vou à praia.

### c) Quando me deito tarde, é necessário que eu durma até o meio-dia

Defina:

- $p$: deito tarde
- $q$: durmo até o meio-dia

Temos:

$$
p \rightarrow q
$$

**Oposta:**

> Eu me deito tarde e não durmo até o meio-dia.

**Contrapositiva:**

> Se eu não durmo até o meio-dia, então não me deito tarde.

**Inversa:**

> Se eu não me deito tarde, então não durmo até o meio-dia.

---

## 2. Tabelas-verdade

### a) $[(p \rightarrow q) \land (q \rightarrow r)] \rightarrow (p \rightarrow r)$

| $p$ | $q$ | $r$ | $p \rightarrow q$ | $q \rightarrow r$ | $(p \rightarrow q) \land (q \rightarrow r)$ | $p \rightarrow r$ | Resultado |
|---|---|---|---|---|---|---|---|
| V | V | V | V | V | V | V | **V** |
| V | V | F | V | F | F | F | **V** |
| V | F | V | F | V | F | V | **V** |
| V | F | F | F | V | F | F | **V** |
| F | V | V | V | V | V | V | **V** |
| F | V | F | V | F | F | V | **V** |
| F | F | V | V | V | V | V | **V** |
| F | F | F | V | V | V | V | **V** |

Como a última coluna é sempre verdadeira:

$$
\boxed{\text{É uma tautologia.}}
$$

### b) $[p \land (p \rightarrow q)] \rightarrow q$

| $p$ | $q$ | $p \rightarrow q$ | $p \land (p \rightarrow q)$ | Resultado |
|---|---|---|---|---|
| V | V | V | V | **V** |
| V | F | F | F | **V** |
| F | V | V | F | **V** |
| F | F | V | F | **V** |

Logo:

$$
\boxed{\text{É uma tautologia.}}
$$

### c) $[(p \lor q) \land (p \rightarrow r) \land (q \rightarrow r)] \rightarrow r$

| $p$ | $q$ | $r$ | $p \lor q$ | $p \rightarrow r$ | $q \rightarrow r$ | Antecedente | Resultado |
|---|---|---|---|---|---|---|---|
| V | V | V | V | V | V | V | **V** |
| V | V | F | V | F | F | F | **V** |
| V | F | V | V | V | V | V | **V** |
| V | F | F | V | F | V | F | **V** |
| F | V | V | V | V | V | V | **V** |
| F | V | F | V | V | F | F | **V** |
| F | F | V | F | V | V | F | **V** |
| F | F | F | F | V | V | F | **V** |

Logo:

$$
\boxed{\text{É uma tautologia.}}
$$

---

## 3. Equivalência lógica entre $p \leftrightarrow q$ e $\neg p \leftrightarrow \neg q$

Começamos com:

$$
p \leftrightarrow q
$$

Pela equivalência do bicondicional:

$$
p \leftrightarrow q
\equiv
(p \rightarrow q) \land (q \rightarrow p)
$$

Usando:

$$
p \rightarrow q \equiv \neg p \lor q
$$

obtemos:

$$
p \leftrightarrow q
\equiv
(\neg p \lor q) \land (\neg q \lor p)
$$

Agora:

$$
\neg p \leftrightarrow \neg q
$$

é equivalente a:

$$
(\neg p \rightarrow \neg q) \land (\neg q \rightarrow \neg p)
$$

Aplicando a equivalência da implicação:

$$
\equiv
(p \lor \neg q) \land (q \lor \neg p)
$$

Pela comutatividade da disjunção:

$$
\equiv
(\neg q \lor p) \land (\neg p \lor q)
$$

que é a mesma expressão obtida anteriormente.

Portanto:

$$
\boxed{
p \leftrightarrow q
\equiv
\neg p \leftrightarrow \neg q
}
$$

---

## 4. Quantificadores

Queremos determinar se:

$$
\forall x(P(x) \leftrightarrow Q(x))
$$

e

$$
(\forall xP(x)) \leftrightarrow (\forall xQ(x))
$$

são logicamente equivalentes.

**Resposta: não são logicamente equivalentes.**

Para demonstrar, basta encontrar um contraexemplo.

Considere o domínio:

$$
D = \{1,2\}
$$

Defina:

$$
P(1)=V,\qquad P(2)=F
$$

e:

$$
Q(1)=F,\qquad Q(2)=V
$$

Então:

$$
P(1)\leftrightarrow Q(1)=F
$$

e:

$$
P(2)\leftrightarrow Q(2)=F
$$

Portanto:

$$
\forall x(P(x)\leftrightarrow Q(x))=F
$$

Por outro lado:

$$
\forall xP(x)=F
$$

e:

$$
\forall xQ(x)=F
$$

Logo:

$$
(\forall xP(x))\leftrightarrow(\forall xQ(x))
=
F\leftrightarrow F
=
V
$$

Encontramos duas proposições com valores-verdade diferentes. Portanto:

$$
\boxed{
\forall x(P(x)\leftrightarrow Q(x))
\not\equiv
(\forall xP(x))\leftrightarrow(\forall xQ(x))
}
$$

---

## 5. Valores-verdade de $Q(x)$

Considere:

$$
Q(x): x+1>2x
$$

com domínio sendo todos os números inteiros.

Simplificando:

$$
x+1>2x
$$

$$
1>x
$$

portanto:

$$
\boxed{x<1}
$$

### a) $Q(0)$

$$
0+1>2(0)
$$

$$
1>0
$$

Verdadeiro.

$$
\boxed{V}
$$

### b) $Q(-1)$

$$
-1+1>2(-1)
$$

$$
0>-2
$$

Verdadeiro.

$$
\boxed{V}
$$

### c) $Q(1)$

$$
1+1>2(1)
$$

$$
2>2
$$

Falso.

$$
\boxed{F}
$$

### d) $\exists xQ(x)$

Existe algum inteiro que satisfaz $x<1$.

Por exemplo, $x=0$.

Logo:

$$
\boxed{V}
$$

### e) $\forall xQ(x)$

Isso afirmaria que todo inteiro satisfaz $x<1$.

Mas $x=1$ não satisfaz.

Logo:

$$
\boxed{F}
$$

### f) $\exists x\neg Q(x)$

Existe algum inteiro que não satisfaz $Q(x)$.

Por exemplo:

$$
x=1
$$

Logo:

$$
\boxed{V}
$$

### g) $\forall x\neg Q(x)$

Isso afirmaria que nenhum inteiro satisfaz $Q(x)$.

Mas $x=0$ satisfaz.

Logo:

$$
\boxed{F}
$$

### Resumo

| Item | Valor-verdade |
|---|---|
| a | **V** |
| b | **V** |
| c | **F** |
| d | **V** |
| e | **F** |
| f | **V** |
| g | **F** |

---

## 6. Negações dos quantificadores

As principais regras utilizadas são:

$$
\neg\exists xP(x)\equiv\forall x\neg P(x)
$$

$$
\neg\forall xP(x)\equiv\exists x\neg P(x)
$$

Além das leis de De Morgan:

$$
\neg(P\land Q)\equiv\neg P\lor\neg Q
$$

$$
\neg(P\lor Q)\equiv\neg P\land\neg Q
$$

### a)

Proposição:

$$
\exists z\forall y\forall xT(x,y,z)
$$

Negando:

$$
\neg\exists z\forall y\forall xT(x,y,z)
$$

Invertendo os quantificadores:

$$
\boxed{
\forall z\exists y\exists x\neg T(x,y,z)
}
$$

### b)

Proposição:

$$
\exists x\exists yP(x,y)
\land
\forall x\forall yQ(x,y)
$$

Negando:

$$
\neg
\left[
\exists x\exists yP(x,y)
\land
\forall x\forall yQ(x,y)
\right]
$$

Pela lei de De Morgan:

$$
\neg\exists x\exists yP(x,y)
\lor
\neg\forall x\forall yQ(x,y)
$$

Portanto:

$$
\boxed{
\forall x\forall y\neg P(x,y)
\lor
\exists x\exists y\neg Q(x,y)
}
$$

### c)

Proposição:

$$
\exists x\exists y
(Q(x,y)\leftrightarrow Q(y,x))
$$

Negando:

$$
\forall x\forall y
\neg(Q(x,y)\leftrightarrow Q(y,x))
$$

A negação do bicondicional pode ser escrita como:

$$
(A\land\neg B)\lor(\neg A\land B)
$$

Assim:

$$
\boxed{
\forall x\forall y
\left[
(Q(x,y)\land\neg Q(y,x))
\lor
(\neg Q(x,y)\land Q(y,x))
\right]
}
$$

### d)

Proposição:

$$
\forall y\exists x\exists z
(T(x,y,z)\lor Q(x,y))
$$

Negando:

$$
\exists y\forall x\forall z
\neg(T(x,y,z)\lor Q(x,y))
$$

Aplicando De Morgan:

$$
\boxed{
\exists y\forall x\forall z
(\neg T(x,y,z)\land\neg Q(x,y))
}
$$

---

## 7. Regras de inferência

Temos as hipóteses:

$$
\forall x(P(x)\lor Q(x))
$$

e:

$$
\forall x((\neg P(x)\land Q(x))\rightarrow R(x))
$$

Queremos demonstrar:

$$
\forall x(\neg R(x)\rightarrow P(x))
$$

Escolhemos um elemento arbitrário $a$ do domínio.

Das hipóteses, temos:

$$
P(a)\lor Q(a)
\tag{1}
$$

e:

$$
(\neg P(a)\land Q(a))\rightarrow R(a)
\tag{2}
$$

Vamos provar:

$$
\neg R(a)\rightarrow P(a)
$$

Suponha:

$$
\neg R(a)
$$

Agora, suponha por contradição que:

$$
\neg P(a)
$$

De (1):

$$
P(a)\lor Q(a)
$$

Como $\neg P(a)$, pelo **silogismo disjuntivo**:

$$
Q(a)
$$

Assim:

$$
\neg P(a)\land Q(a)
$$

Pela hipótese (2):

$$
R(a)
$$

Mas havíamos assumido:

$$
\neg R(a)
$$

Temos uma contradição.

Portanto:

$$
P(a)
$$

Como $a$ foi escolhido arbitrariamente:

$$
\boxed{
\forall x(\neg R(x)\rightarrow P(x))
}
$$

---

## 8. Resolução

Defina:

- $A$: Allen é um garoto mau.
- $H$: Hillary é uma boa garota.
- $D$: David é feliz.

As hipóteses são:

> Allen é um garoto mau ou Hillary é uma boa garota.

Formalmente:

$$
A\lor H
$$

E:

> Allen é um bom garoto ou David é feliz.

Como "Allen é um bom garoto" é a negação de "Allen é um garoto mau":

$$
\neg A\lor D
$$

Queremos demonstrar:

$$
H\lor D
$$

Aplicando a regra de resolução:

$$
\frac{A\lor H \qquad \neg A\lor D}{H\lor D}
$$

Eliminamos $A$ e $\neg A$ e obtemos:

$$
\boxed{H\lor D}
$$

Portanto, a conclusão segue das hipóteses.

---

## 9. Inverso aditivo de um número par

Seja $n$ um número par.

Pela definição de número par, existe $k\in\mathbb{Z}$ tal que:

$$
n=2k
$$

O inverso aditivo de $n$ é:

$$
-n
$$

Substituindo $n=2k$:

$$
-n=-2k
$$

Podemos escrever:

$$
-n=2(-k)
$$

Como:

$$
k\in\mathbb{Z}
$$

então:

$$
-k\in\mathbb{Z}
$$

Logo, $-n$ é divisível por $2$.

Portanto:

$$
\boxed{
\text{O inverso aditivo de um número par é par.}
}
$$

---

## 10. Se $m$ e $n$ são inteiros e $mn$ é par, então $m$ é par ou $n$ é par

Queremos demonstrar:

$$
mn\text{ é par}
\rightarrow
(m\text{ é par}\lor n\text{ é par})
$$

Uma forma conveniente é provar a **contrapositiva**:

$$
(m\text{ não é par})\land(n\text{ não é par})
\rightarrow
mn\text{ não é par}
$$

Se um número inteiro não é par, então ele é ímpar.

Logo, podemos escrever:

$$
m=2a+1
$$

e:

$$
n=2b+1
$$

para algum $a,b\in\mathbb{Z}$.

Multiplicando:

$$
mn=(2a+1)(2b+1)
$$

Distribuindo:

$$
mn=4ab+2a+2b+1
$$

Colocando $2$ em evidência:

$$
mn=2(2ab+a+b)+1
$$

Essa é a forma geral de um número ímpar:

$$
2k+1
$$

Logo, $mn$ é ímpar.

Assim:

$$
m,n\text{ ímpares}
\rightarrow
mn\text{ ímpar}
$$

Pela contrapositiva:

$$
\boxed{
mn\text{ par}
\rightarrow
m\text{ par ou }n\text{ par}
}
$$

Portanto, se o produto de dois inteiros é par, pelo menos um dos fatores é par.
