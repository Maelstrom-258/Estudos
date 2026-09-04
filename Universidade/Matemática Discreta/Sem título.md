Bora. A lista tem 10 questões, cobrindo lógica proposicional, quantificadores, regras de inferência, resolução e demonstrações matemáticas. Vou resolver na ordem, mostrando o raciocínio para você conseguir acompanhar.

### 1. Oposta, contrapositiva e inversa

Para uma condicional:

> Se pp, então qq.

Temos:

- **Oposta (negação):** p∧¬qp \land \neg q
    
- **Contrapositiva:** ¬q→¬p\neg q \rightarrow \neg p
    
- **Inversa:** ¬p→¬q\neg p \rightarrow \neg q
    

#### a) Se nevar esta noite, então ficarei em casa.

Defina:

pp: nevar esta noite  
qq: ficarei em casa

**Oposta:**

> Neva esta noite e eu não fico em casa.

**Contrapositiva:**

> Se eu não ficar em casa, então não nevará esta noite.

**Inversa:**

> Se não nevar esta noite, então não ficarei em casa.

---

#### b) Eu vou à praia sempre que faz um dia ensolarado de verão.

" pp sempre que qq" significa q→pq \rightarrow p.

pp: vou à praia  
qq: faz um dia ensolarado de verão

Logo:

**Oposta:**

> Faz um dia ensolarado de verão e eu não vou à praia.

**Contrapositiva:**

> Se eu não vou à praia, então não faz um dia ensolarado de verão.

**Inversa:**

> Se não faz um dia ensolarado de verão, então eu não vou à praia.

---

#### c) Quando me deito tarde, é necessário que eu durma até o meio-dia.

pp: deito tarde  
qq: durmo até o meio-dia

Temos p→qp \rightarrow q.

**Oposta:**

> Eu me deito tarde e não durmo até o meio-dia.

**Contrapositiva:**

> Se eu não durmo até o meio-dia, então não me deito tarde.

**Inversa:**

> Se eu não me deito tarde, então não durmo até o meio-dia.

---

# 2. Tabelas-verdade

A lista pede que as três proposições sejam demonstradas como tautologias usando tabela-verdade.

### a) [(p→q)∧(q→r)]→(p→r)[(p\rightarrow q)\land(q\rightarrow r)]\rightarrow(p\rightarrow r)

Tabela:

|pp|qq|rr|p→qp\to q|q→rq\to r|conjunção|p→rp\to r|resultado|
|---|---|---|---|---|---|---|---|
|V|V|V|V|V|V|V|**V**|
|V|V|F|V|F|F|F|**V**|
|V|F|V|F|V|F|V|**V**|
|V|F|F|F|V|F|F|**V**|
|F|V|V|V|V|V|V|**V**|
|F|V|F|V|F|F|V|**V**|
|F|F|V|V|V|V|V|**V**|
|F|F|F|V|V|V|V|**V**|

A última coluna é sempre V.

**Logo, é uma tautologia.**

---

### b) [p∧(p→q)]→q[p\land(p\rightarrow q)]\rightarrow q

|pp|qq|p→qp\to q|p∧(p→q)p\land(p\to q)|resultado|
|---|---|---|---|---|
|V|V|V|V|**V**|
|V|F|F|F|**V**|
|F|V|V|F|**V**|
|F|F|V|F|**V**|

**Tautologia.**

---

### c) [(p∨q)∧(p→r)∧(q→r)]→r[(p\lor q)\land(p\to r)\land(q\to r)]\to r

|pp|qq|rr|p∨qp\lor q|p→rp\to r|q→rq\to r|antecedente|resultado|
|---|---|---|---|---|---|---|---|
|V|V|V|V|V|V|V|**V**|
|V|V|F|V|F|F|F|**V**|
|V|F|V|V|V|V|V|**V**|
|V|F|F|V|F|V|F|**V**|
|F|V|V|V|V|V|V|**V**|
|F|V|F|V|V|F|F|**V**|
|F|F|V|F|V|V|F|**V**|
|F|F|F|F|V|V|F|**V**|

Também é uma **tautologia**.

---

# 3. Mostrar que p↔qp\leftrightarrow q e ¬p↔¬q\neg p\leftrightarrow\neg q são logicamente equivalentes

A questão pede uma demonstração por equivalências lógicas.

Começamos:

p↔qp\leftrightarrow q

Pela equivalência:

p↔q≡(p→q)∧(q→p)p\leftrightarrow q\equiv(p\rightarrow q)\land(q\rightarrow p)

Substituindo implicações:

≡(¬p∨q)∧(¬q∨p)\equiv(\neg p\lor q)\land(\neg q\lor p)

Agora:

¬p↔¬q\neg p\leftrightarrow\neg q ≡(¬p→¬q)∧(¬q→¬p)\equiv(\neg p\rightarrow\neg q)\land(\neg q\rightarrow\neg p)

Usando p→q≡¬p∨qp\rightarrow q\equiv\neg p\lor q:

≡(p∨¬q)∧(q∨¬p)\equiv(p\lor\neg q)\land(q\lor\neg p)

Pela comutatividade da disjunção:

≡(¬q∨p)∧(¬p∨q)\equiv(\neg q\lor p)\land(\neg p\lor q)

Que é exatamente:

(¬p∨q)∧(¬q∨p)(\neg p\lor q)\land(\neg q\lor p)

Portanto:

p↔q≡¬p↔¬q\boxed{p\leftrightarrow q\equiv\neg p\leftrightarrow\neg q}

---

# 4. Quantificadores

A questão pergunta se

∀x(P(x)↔Q(x))\forall x(P(x)\leftrightarrow Q(x))

e

(∀xP(x))↔(∀xQ(x))(\forall xP(x))\leftrightarrow(\forall xQ(x))

são logicamente equivalentes.

**Não são.**

Para mostrar isso, basta encontrar um contraexemplo.

Considere o domínio:

D={1,2}D=\{1,2\}

Defina:

P(1)=V,P(2)=FP(1)=V,\quad P(2)=F

e

Q(1)=V,Q(2)=VQ(1)=V,\quad Q(2)=V

Então:

P(1)↔Q(1)=VP(1)\leftrightarrow Q(1)=V

mas:

P(2)↔Q(2)=FP(2)\leftrightarrow Q(2)=F

Portanto:

∀x(P(x)↔Q(x))=F\forall x(P(x)\leftrightarrow Q(x))=F

Agora:

∀xP(x)=F\forall xP(x)=F

e

∀xQ(x)=V\forall xQ(x)=V

Logo:

(∀xP(x))↔(∀xQ(x))(\forall xP(x))\leftrightarrow(\forall xQ(x))

é:

F↔V=FF\leftrightarrow V=F

Esse exemplo não diferencia as duas, então precisamos de um exemplo melhor.

Considere:

P(1)=V,P(2)=FP(1)=V,\quad P(2)=F Q(1)=F,Q(2)=VQ(1)=F,\quad Q(2)=V

Temos:

∀x(P(x)↔Q(x))=F\forall x(P(x)\leftrightarrow Q(x))=F

pois em ambos os elementos PP e QQ possuem valores diferentes.

Por outro lado:

∀xP(x)=F\forall xP(x)=F

e

∀xQ(x)=F\forall xQ(x)=F

Logo:

F↔F=VF\leftrightarrow F=V

Assim:

∀x(P(x)↔Q(x))≢(∀xP(x))↔(∀xQ(x))\boxed{\forall x(P(x)\leftrightarrow Q(x))\not\equiv (\forall xP(x))\leftrightarrow(\forall xQ(x))}

---

# 5. Q(x):x+1>2xQ(x):x+1>2x

A questão define Q(x)Q(x) e diz que o domínio é o conjunto dos inteiros.

Primeiro vamos simplificar:

x+1>2xx+1>2x 1>x1>x

ou seja:

x<1\boxed{x<1}

### a) Q(0)Q(0)

0+1>2(0)0+1>2(0) 1>01>0

Verdadeiro.

V\boxed{V}

### b) Q(−1)Q(-1)

−1+1>2(−1)-1+1>2(-1) 0>−20>-2

Verdadeiro.

V\boxed{V}

### c) Q(1)Q(1)

1+1>2(1)1+1>2(1) 2>22>2

Falso.

F\boxed{F}

### d) ∃xQ(x)\exists xQ(x)

Existe algum inteiro x<1x<1.

Por exemplo:

x=0x=0

Logo:

V\boxed{V}

### e) ∀xQ(x)\forall xQ(x)

Isso afirmaria que todo inteiro satisfaz x<1x<1.

Falso. Por exemplo:

x=1x=1

não satisfaz.

F\boxed{F}

### f) ∃x¬Q(x)\exists x\neg Q(x)

Existe algum inteiro para o qual x≥1x\geq1.

Por exemplo:

x=1x=1

Logo:

V\boxed{V}

### g) ∀x¬Q(x)\forall x\neg Q(x)

Isso significa que nenhum inteiro satisfaz x<1x<1.

Mas 0<10<1, por exemplo.

F\boxed{F}

Portanto:

|Item|Valor|
|---|---|
|a|**V**|
|b|**V**|
|c|**F**|
|d|**V**|
|e|**F**|
|f|**V**|
|g|**F**|

---

# 6. Negações dos quantificadores

A regra fundamental é:

¬∃xP(x)≡∀x¬P(x)\neg\exists xP(x)\equiv\forall x\neg P(x) ¬∀xP(x)≡∃x¬P(x)\neg\forall xP(x)\equiv\exists x\neg P(x)

E:

¬(P∧Q)≡¬P∨¬Q\neg(P\land Q)\equiv\neg P\lor\neg Q ¬(P∨Q)≡¬P∧¬Q\neg(P\lor Q)\equiv\neg P\land\neg Q

A lista pede que as negações fiquem imediatamente antes dos predicados.

### a)

∃z∀y∀xT(x,y,z)\exists z\forall y\forall xT(x,y,z)

Negando:

¬∃z∀y∀xT(x,y,z)\neg\exists z\forall y\forall xT(x,y,z)

Troca os quantificadores:

∀z∃y∃x¬T(x,y,z)\boxed{\forall z\exists y\exists x\neg T(x,y,z)}

---

### b)

∃x∃yP(x,y)∧∀x∀yQ(x,y)\exists x\exists yP(x,y)\land\forall x\forall yQ(x,y)

Negamos cada parte:

¬[∃x∃yP(x,y)∧∀x∀yQ(x,y)]\neg\left[ \exists x\exists yP(x,y) \land \forall x\forall yQ(x,y) \right]

Pela lei de De Morgan:

¬∃x∃yP(x,y)∨¬∀x∀yQ(x,y)\neg\exists x\exists yP(x,y) \lor \neg\forall x\forall yQ(x,y)

Logo:

∀x∀y¬P(x,y)∨∃x∃y¬Q(x,y)\boxed{ \forall x\forall y\neg P(x,y) \lor \exists x\exists y\neg Q(x,y) }

---

### c)

∃x∃y(Q(x,y)↔Q(y,x))\exists x\exists y(Q(x,y)\leftrightarrow Q(y,x))

Negando:

∀x∀y¬(Q(x,y)↔Q(y,x))\forall x\forall y \neg(Q(x,y)\leftrightarrow Q(y,x))

Podemos escrever a negação do bicondicional como:

(A∧¬B)∨(¬A∧B)(A\land\neg B)\lor(\neg A\land B)

Então:

∀x∀y[(Q(x,y)∧¬Q(y,x))∨(¬Q(x,y)∧Q(y,x))]\boxed{ \forall x\forall y[ (Q(x,y)\land\neg Q(y,x)) \lor (\neg Q(x,y)\land Q(y,x)) ] }

---

### d)

∀y∃x∃z(T(x,y,z)∨Q(x,y))\forall y\exists x\exists z (T(x,y,z)\lor Q(x,y))

Negando:

∃y∀x∀z¬(T(x,y,z)∨Q(x,y))\exists y\forall x\forall z \neg(T(x,y,z)\lor Q(x,y))

De Morgan:

∃y∀x∀z(¬T(x,y,z)∧¬Q(x,y))\boxed{ \exists y\forall x\forall z (\neg T(x,y,z)\land\neg Q(x,y)) }

---

# 7. Regras de inferência

Temos:

∀x(P(x)∨Q(x))\forall x(P(x)\lor Q(x))

e

∀x((¬P(x)∧Q(x))→R(x))\forall x((\neg P(x)\land Q(x))\rightarrow R(x))

Queremos provar:

∀x(¬R(x)→P(x))\forall x(\neg R(x)\rightarrow P(x))

Isso está na questão 7 da lista.

Pegamos um elemento arbitrário aa.

Das hipóteses:

P(a)∨Q(a)(1)P(a)\lor Q(a) \tag{1}

e

(¬P(a)∧Q(a))→R(a)(2)(\neg P(a)\land Q(a))\rightarrow R(a) \tag{2}

Queremos:

¬R(a)→P(a)\neg R(a)\rightarrow P(a)

Aplicando a contrapositiva em (2):

¬R(a)→¬(¬P(a)∧Q(a))\neg R(a)\rightarrow \neg(\neg P(a)\land Q(a))

De Morgan:

¬R(a)→(P(a)∨¬Q(a))\neg R(a)\rightarrow(P(a)\lor\neg Q(a))

Agora suponha:

¬R(a)\neg R(a)

Então:

P(a)∨¬Q(a)(3)P(a)\lor\neg Q(a) \tag{3}

Temos também:

P(a)∨Q(a)(1)P(a)\lor Q(a) \tag{1}

Isso, sozinho, não permite concluir P(a)P(a). Portanto vamos usar uma prova por contradição.

Suponha:

¬P(a)\neg P(a)

De (1):

P(a)∨Q(a)P(a)\lor Q(a)

Como ¬P(a)\neg P(a), pelo **silogismo disjuntivo**:

Q(a)Q(a)

Portanto:

¬P(a)∧Q(a)\neg P(a)\land Q(a)

Pela hipótese (2):

R(a)R(a)

Mas inicialmente tínhamos:

¬R(a)\neg R(a)

Contradição.

Logo:

P(a)P(a)

Portanto:

∀x(¬R(x)→P(x))\boxed{\forall x(\neg R(x)\rightarrow P(x))}

---

# 8. Resolução

Hipóteses:

> Allen é um garoto mau ou Hillary é uma boa garota.

Defina:

AA: Allen é um garoto mau  
HH: Hillary é uma boa garota  
DD: David é feliz

Primeira hipótese:

A∨HA\lor H

Segunda:

> Allen é um bom garoto ou David é feliz.

"Allen é um bom garoto" é ¬A\neg A, portanto:

¬A∨D\neg A\lor D

Queremos:

H∨DH\lor D

Agora aplicamos **resolução**:

A∨HA\lor H ¬A∨D\neg A\lor D

Eliminamos AA e ¬A\neg A:

H∨D\boxed{H\lor D}

Que é exatamente a conclusão.

---

# 9. Inverso aditivo de um número par

A questão pede uma demonstração direta.

Seja nn um número par.

Pela definição de número par:

n=2kn=2k

para algum inteiro kk.

O inverso aditivo de nn é:

−n-n

Como:

n=2kn=2k

temos:

−n=−2k-n=-2k

Colocando 22 em evidência:

−n=2(−k)-n=2(-k)

Como k∈Zk\in\mathbb Z, então:

−k∈Z-k\in\mathbb Z

Logo, −n-n é divisível por 2.

Portanto:

O inverso aditivo de um nuˊmero par eˊ par.\boxed{\text{O inverso aditivo de um número par é par.}}

---

# 10. Se mnmn é par, então mm é par ou nn é par

A questão pede exatamente essa demonstração.

Queremos provar:

mn eˊ par⇒(m eˊ par∨n eˊ par)mn\text{ é par}\Rightarrow (m\text{ é par}\lor n\text{ é par})

Aqui a maneira mais limpa é usar a **contrapositiva**.

A contrapositiva é:

m na˜o eˊ par∧n na˜o eˊ par⇒mn na˜o eˊ parm\text{ não é par}\land n\text{ não é par} \Rightarrow mn\text{ não é par}

Se um número inteiro não é par, ele é ímpar.

Então podemos escrever:

m=2a+1m=2a+1

e

n=2b+1n=2b+1

para a,b∈Za,b\in\mathbb Z.

Multiplicando:

mn=(2a+1)(2b+1)mn=(2a+1)(2b+1)

Distribuindo:

mn=4ab+2a+2b+1mn=4ab+2a+2b+1

Colocando 2 em evidência:

mn=2(2ab+a+b)+1mn=2(2ab+a+b)+1

Isso possui a forma:

2k+12k+1

Portanto mnmn é **ímpar**.

Assim, mostramos:

m,n ıˊmpares⇒mn ıˊmparm,n\text{ ímpares}\Rightarrow mn\text{ ímpar}

Pela contrapositiva:

mn par⇒m par ou n par\boxed{mn\text{ par}\Rightarrow m\text{ par ou }n\text{ par}}

Essa é a resolução completa da lista, seguindo os enunciados do PDF.