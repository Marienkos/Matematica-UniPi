# Asserzioni
Si dice preposizione una frase avente valore di verità vero o falso.

Le possibili operazioni sono: negazione, and, or, xor, implicazione

Si dice predicato una proposizione parametrizzata tramite quantificatori.

I possibili quantificatori sono: per ogni, esiste almeno un, esiste ed è unico.

$\neg(\forall x$   $P(x))$ è come dire $\exists x$   $\neg P(x)$ e viceversa.

Sia $P(n)$ un predicato su $\mathbb N$. Se valgono:
1. $P(n_0)$
2. $P(n) \implies P(n+1)$
Allora $\forall n>n_0$   $P(n)$ e si dice che vale per induzione.

# Insiemi
Gli insiemi possono essere presentati:
- per elenco: A = {2, 4, 6, ...}
- per proprietà: A = {n : "n è un numero pari"}

Le operazioni possibili sono: unione, intersezione, differenza, prodotto cartesiano.

# Numeri naturali
I numeri naturali sono l'unica tupla $(\mathbb{N},0,s)$ a meno di isomorfismi, dove:
- $\mathbb{N}$ è un insieme
- $0 \in \mathbb{N}$
- $s : \mathbb{N} \to \mathbb{N}$ tale che:
	1. $s$ iniettiva
	2. $s(\mathbb{N})=\mathbb{N} \setminus \{ 0 \}$
	3. $\forall A \subseteq \mathbb{N}$ se $0 \in A$ e $\forall n \in \mathbb{N}$   $n \in A \implies s(n) \in A$, allora $A = \mathbb{N}$

La somma è definita come $+ : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ tale che:
1. $a + 0 = a$
2. $a + s(n) = s(a+n)$

Il prodotto è definito come $* : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ tale che:
1. $a*0 = 0$
2. $a * s(n) = a*n+a$

# Numeri interi relativi
Dato $\mathbb{N} \times \mathbb{N}$, si considera la relazione $(n_{1},m_{1}) \sim (n_{2},m_{2}) \iff n_{1}+m_{2}=n_{2}+m_{1}$.

Si dimostra che la relazione di cui sopra è una relazione di equivalenza.

L'insieme dei numeri interi relativi è $\mathbb{Z} := \frac{{\mathbb{N}\times \mathbb{N}}}{\sim}$.

La somma è definita come $+ : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$ data da $(a_{1},b_{1})+(a_{2},b_{2})=(a_{1}+a_{2},b_{1}+b_{2})$.

Il prodotto è definito come $* : \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$ dato da $(a_{1},b_{1}) * (a_{2},b_{2}) =  (a_{1}a_{2}+b_{1}b_{2},a_{1}b_{2} + a_{2}b_{1})$.

# Numeri razionali
Data $(a,b) \in\mathbb{Z} \times \mathbb{Z}$ con $b \neq 0$, si considera la relazione $(a,b) \sim (\hat{a},\hat{b}) \iff a\hat{b} = \hat{a}b$.

Si dimostra che la relazione di cui sopra è una relazione di equivalenza.

L'insieme dei numeri razionali è $\mathbb{Q} := \frac{{\mathbb{Z} \times \mathbb{Z}}}{\sim}$.

La somma è definita come $+ : \mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ data da $(a,b)+(c,d)=(ad+bc,bd)$.

Il prodotto è definito come $* : \mathbb{Q} \times \mathbb{Q} \to \mathbb{Q}$ dato da $(a,b)*(c,d)=(ac,bd)$.

# Numeri reali (definizione assiomatica)
I numeri reali sono l'unica tupla $(\mathbb R, +, *, \geq)$ a meno di isomorfismi, dove:
- $+,* : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ sono rispettivamente somma e prodotto
- (Assiomi algebrici) $\mathbb R$ è un campo rispetto alle due operazioni con almeno due elementi
- (Assiomi di ordinamento) $\geq$ è un ordinamento totale e le due operazioni non alterano il verso
- Vale l'assioma di continuità

Dati $A \subseteq \mathbb R$ e $B \subseteq \mathbb R$ non vuoti, A sta a sinistra di B se $\forall a \in A$   $\forall b \in B$   $a \leq b$

- (Assioma di continuità) Se A sta a sinistra di B, allora $\exists c \in \mathbb R$   $a \leq c$   $\forall a \in A$   $\land c \leq b$   $\forall b \in B$

In $\mathbb{R}$ sono detti insiemi connessi e/o convessi $\emptyset$, i punti, gli intervalli con o senza estremi, le semirette e $\mathbb{R}$ stesso.

# Maggioranti e minoranti
Un maggiorante di A è maggiore di ogni elemento di A. Al contrario per il minorante.

Un maggiorante è detto massimo se appartiene ad A. Il minorante è detto minimo.

L'estremo superiore di A, anche detto $\sup A$, è $+\infty$ se non esistono maggioranti, altrimenti è il minimo maggiorante. Al contrario per l'estremo inferiore, anche detto $\inf A$.

Sia $A \subseteq \mathbb{R}$. Allora inf e sup esistono sempre.

~={orange}DIMOSTRAZIONE=~
- Se non ci sono maggioranti, allora il sup esiste.
- Se ci sono maggioranti, chiamiamo B il loro insieme. B sta a destra di A, dunque per l'assioma di continuità esiste un c minimo di B, ossia il sup di A.

# Numeri reali (sezioni di Dedekind)
Si dice semiretta sinistra un sottoinsieme $A \subseteq \mathbb{Q}$ tale che:
1. $A$ ammette almeno un maggiorante
2. $a \in A \land b \leq a \implies b \in A$
3. $A$ non ammette massimo

Si definisce l'insieme dei numeri reali $\mathbb{R} := \{ \text{semirette sinistre di } \mathbb{Q} \}$.

Si definiscono le operazioni $+,* : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ di somma e prodotto.

Si verifica che la definizione a sezioni di Dedekind è equivalente a quella assiomatica, in particolare:
- $\mathbb{R}$ è un campo rispetto alle operazioni
- si può definire l'ordinamento come l'inclusione insiemistica di semirette
- l'assioma di continuità deriva dall'osservazione che il sup è il reale dell'unione

# Esistenza e unicità dei reali
$\mathbb{R}$ esiste.

~={cyan}DIMOSTRAZIONE=~: Sezioni di Dedekind e verifiche.

La tupla $(\mathbb{R}, \leq)$ è unica a meno di isomorfismi.

~={cyan}DIMOSTRAZIONE=~:
1. L'ipotesi si può scrivere come: se $\exists(\hat{\mathbb{R}},\hat{\leq})$ con le stesse proprietà, allora $\exists\varphi : \mathbb{R} \to \hat{\mathbb{R}}$ tale che:
	1. $\varphi$ bigettiva
	2. $\varphi$ isomorfismo di campi
	3. $x \leq y \implies \varphi(x) \hat{\leq} \varphi(y)$
2. Si definiscono $\varphi(0)=\hat{0}$ e $\varphi(1)=\hat{1}$
3. Si considerano $\mathbb{N},\mathbb{Z},\mathbb{Q} \subseteq \mathbb{R}$
4. Si pone $\varphi(n)=\hat{n}$
5. Si estende $\varphi$ all'immagine di $\mathbb{Z}$ e $\mathbb{Q}$
6. Si mostra che $\varphi$ manda semirette sinistre di $\mathbb{Q}$ in semirette sinistre di $\hat{\mathbb{Q}}$

# Funzione
Una funzione $f : A \rightarrow B$ è un insieme di partenza, uno di arrivo e una legge che associa a ogni elemento di $A$ un unico elemento di $B$, indicato con $f(a)$.

Il grafico è un sottoinsieme del prodotto cartesiano definito dalla legge per proprietà.

Una funzione è un sottoinsieme del prodotto cartesiano tale che per ogni $a \in A$ esiste un solo $b \in B$ in esso.

Due funzioni sono uguali se lo sono in ogni punto.

Se una funzione è nulla in tutto il suo insieme di definizione, allora si dice che è identicamente nulla e si scrive $f(x) \equiv 0$.

Date due funzioni $f : A \rightarrow B$ e $g : B \rightarrow C$, si definisce $(g \circ f)(a) = g(f(a))$.

Una funzione $f : A \rightarrow B$ è:
- iniettiva se $a_1 \neq a_2 \implies f(a_1) \neq f(a_2)$
- surgettiva se $\forall b \in B$   $\exists a \in A$   $b = f(a)$
- bigettiva se iniettiva e surgettiva
- pari se $f(x) = f(-x)$
- dispari se $f(-x) = -f(x)$
- periodica se $\exists p$   $f(x+p) = f(x)$
- monotona se $x > y \implies f(x)$   $\{>, \geq, <, \leq\}$   $f(y)$

In questi appunti si userà la notazione $\Delta_{a}^b f = f(a)-f(b)$.

# Inversa
Data una funzione $f : A \rightarrow B$, una funzione $g : B \rightarrow A$ è detta:
- inversa sinistra di $f$ se $g \circ f = id$
- inversa destra di $f$ se $f \circ g = id$
- inversa di $f$ se è sia inversa sinistra che destra

Per ogni funzione valgono:
- invertibile a sinistra $\iff$ iniettiva
- invertibile a destra $\iff$ surgettiva

# Funzione razionale
Partendo dall'anello dei polinomi $\mathbb{R}[x]$ si può estendere a campo su cui si può definire una relazione d'ordine $\frac{P_{1}(x)}{Q_{1}(x)}\geq \frac{P_{2}(x)}{Q_{2}(x)} \iff$ la disuguaglianza vale per $x$ abbastanza grandi.

La relazione d'ordine è compatibile con le operazioni.

In $\mathbb{R}[x]$ non vale l'assioma di continuità ed equivalenti.

~={cyan}DIMOSTRAZIONE=~: Si verifica che niente sta tra le costanti e i monomi di primo grado.