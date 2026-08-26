# Anello
Un anello con unità $R$ è un insieme dotato di due operazioni binarie tale che:
1. $R$ è un gruppo rispetto alle due operazioni $+$ e $\cdot$
2. la moltiplicazione è associativa
3. entrambe le operazioni sono distributive

L'elemento neutro rispetto alla somma $0$ e l'elemento neutro rispetto al prodotto $1$ sono unici.

Un anello non deve avere l'$1$, ma per convenzione indicheremo così gli anelli con unità.

Un anello si dice commutativo se vale la commutatività della moltiplicazione.

Sia $R$ anello commutativo. $a \in R$ si dice divisore di zero se $\exists b \in R$   $b \neq 0$   $ab=0$.

Sia $R$ anello. $u \in \mathbb{R}$ si dice invertibile se $\exists v \in R$   $uv=vu=1$.

Sia $R$ anello, allora l'insieme $R^*$ dei suoi invertibili è un gruppo rispetto alla moltiplicazione.

Sia $R$ anello commutativo. $a,b \in R$ si dicono associati se $\exists u \in R^*$   $a=bu$.

Un anello si dice:
- dominio di integrità se l'unico divisore di zero è $0$
- corpo se non banale e ogni elemento non nullo è invertibile
- campo se corpo commutativo

Dato un anello $A$ valgono:
1. $a 0 = 0a=0$
2. L'opposto di $a$ è unico e $-(-a)=a$
3. $a(-b)=(-a)b=-(ab)$
4. $(-a)(-b)=ab$

DIMOSTRAZIONE:
1. $a0 = a(0+0)=a 0 + a 0 = 0$
2. Vale per i gruppi
3. $ab + a(-b) = a(b + (-b)) = a 0 = 0$
4. $(-a)(-b)=-(a(-b))=-(-(ab))=ab$

Campo $\implies$ dominio

DIMOSTRAZIONE: Proprietà precedenti.

# Sottoanello
Siano $R$ anello, $T \subseteq R$ si dice sottoanello se:
1. $1 \in T$
2. $T < R$ visto come gruppo rispetto a $+$
3. $ab \in T$   $\forall a,b \in T$

# Omomorfismo
Siano $R,S$ anelli, $\phi : R \to S$ si dice omomorfismo di anelli $\iff$ valgono:
1. $\phi(a+b)=\phi(a)+\phi(b)$
2. $\phi(ab)=\phi(a)\phi(b)$
3. $\phi(1_{R})=1_{S}$

Le definizioni e le proprietà degli omomorfismi per gruppi si estendono agli anelli.

# $\mathbb{Z}_{p}$
Si indica con $\mathbb{Z}_{p}$ l'insieme delle classi di resto della divisione per $p$.

$p$ primo $\implies \mathbb{Z}_{p}$ campo

DIMOSTRAZIONE: $\mathbb{Z}_{p}$ commutativo, ogni elemento non nullo è invertibile.

# Anello di polinomi a coefficienti in un campo
Sia $K$ campo e $K[x]$ l'insieme dei polinomi nella variabile $x$ a coefficienti in $K$. Allora ogni suo elemento è nella forma $f(x)=a_{n}x^n+\dots+a_{0}$. In tal caso:
- $a_{n}$ è il coefficiente direttore
- $n$ è il grado del polinomio e si scrive $\text{deg}(f(x))$ e $\text{deg}(0)=-\infty$

Siano $f(x),g(x) \in K[x]$, allora $\text{deg}(f(x)g(x)) = \text{deg}(f(x)) + \text{deg}(g(x))$.

Se il coefficiente direttore è $1$, il polinomio è monico.

In $K[x]$ vale la divisione euclidea. Sono definibili massimo comun divisore e vale Bézout.

Sia $L$ campo e $f(x) \in L[x]$ un polinomio di grado $n>0$. Allora $f(x)$ ha al più $n$ radici distinte.

DIMOSTRAZIONE:
- Se $f(x)$ non ha radici, l'enunciato è vero
- Se $f(x)$ ha una radice $\alpha_{1}$, allora $f(x)=(x-\alpha_{1})f_{1}(x)$ e per assurdo non ce ne sono più di $n$.

# Sottogruppo moltiplicativo di un campo
Sia $K$ campo e $G < K^*$ finito, allora $G$ ciclico.

DIMOSTRAZIONE:
- Se $|G|=1$ l'enunciato è banale
- Sia $|G| > 1$
	1. Per ogni $n$ vale $\sum\limits_{d | n} \phi(d)=n$
	2. Sia $X_{d}=\{ a \in G : o(a)=d \}$, vale $\sum\limits_{d | n} |X_{d}|=n$
	3. Se $G$ non ciclico, allora $|X_{n}|=0$, assurdo.

# Numero complesso
Un numero complesso è un elemento dell'insieme $\mathbb{C} := \{ a+ib : a,b\in \mathbb{R} \}$ con $i$, detta unità immaginaria, tale che $i^2=-1$.

Ogni numero complesso è rappresentabile in forma:
- cartesiana, come $a+ib$
- polare, come $r\cos \theta+ir\sin \theta$
- esponenziale, come $e^{i\theta}$

Somma e prodotto sono definiti nel modo polinomiale classico, trattando $i$ come variabile.

Dato $z=a+ib$, si definisce il suo coniugato $\bar{z} = a-ib$.

Valgono:
- $\overline{z+w} = \bar{z} + \bar{w}$
- $\overline{zw}=\bar{z}\bar{w}$
- $z\bar{z}=|z|^2$

Dalle proprietà precedenti consegue che $\mathbb{C}$ è un campo.

Ogni polinomio $f(x)\in \mathbb{C}[x]$ di grado $n$ ha esattamente $n$ radici in $\mathbb{C}$.

Se $f(x) \in \mathbb{C}[x]$ ha una radice $x_{0}$, allora anche $\overline{x_{0}}$ è una radice.

Ogni polinomio $f(x)\in \mathbb{R}[x]$ di grado positivo si fattorizza in $\mathbb{R}[x]$ in fattori di grado $\leq 2$.

# Ideale
Un ideale $I$ è $I < R$ additivo tale che $\forall r \in R$   $\forall h \in I$   $rh \in I$   $hr \in I$.

Un ideale $I$ non è un sottoanello di $R$, tranne se $I=R$.

Sia $R$ anello commutativo e $a \in R$, si dice ideale generato $(a) = \{ ra : r \in R \}$.

Se un ideale è monogenerato, si dice principale.

Il nucleo di un omomorfismo è un ideale.

Se $I,J$ sono ideali, anche $I+J=\{ i+j:i \in I, j \in J \}$, $I \cap J$ e $IJ$ sono ideali. Inoltre $IJ \subseteq I \cap J$.

Si possono estendere quoziente, teorema di omomorfismo e proiezione agli anelli.

Si dice omomorfismo di valutazione $V_{r} : A[x] \to R$ tale che $V_{r}(f(x)) := f(r)$.

Vale $\mathbb{R}[x] / (x^2+1) \cong \mathbb{C}$.

# Quoziente di anelli di polinomi
Sia $K$ campo e $f(x) \in K[x]$ di grado $\geq 1$. Allora $f(x)$ si dice irriducibile se gli unici divisori di $f(x)$ sono i polinomi costanti $\neq 0$ e i polinomi associati a $f(x)$.

Sia $K$ campo e $f(x) \in K[x]$. Allora $K[x] / (f(x))$ campo $\iff f(x)$ irriducibile.

DIMOSTRAZIONE:
1. Sia $f(x)$ irriducibile e $I = (f(x))$
2. $a(x) + I \in K[x] / I$ con $a(x) \neq 0 \implies a(x)+I$ ammette inverso
	1. $\text{MCD}(a(x),f(x))=1$ per irriducibilità
	2. Per Bézout $\exists \lambda(x),\mu(x) \in K[x]$   $a(x)\lambda(x) + f(x)\mu(x)=1$
	3. Si nota che $\lambda(x)+I$ è l'inverso cercato
3. $f(x)$ riducibile $\implies f(x) = 0 \lor$ ha grado $0 \lor f(x)$ si fattorizza $\implies K[x] / I$ non campo