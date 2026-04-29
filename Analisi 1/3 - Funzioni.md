# Definizioni
Una funzione $f : A \rightarrow B$ è un insieme di partenza, uno di arrivo e una legge che associa a ogni elemento di $A$ un unico elemento di $B$, indicato con $f(a)$.

Il grafico è un sottoinsieme del prodotto cartesiano definito dalla legge per proprietà.

Una funzione è un sottoinsieme del prodotto cartesiano tale che per ogni $a \in A$ esiste un solo $b \in B$ in esso.

Due funzioni sono uguali se lo sono in ogni punto.

Date due funzioni $f : A \rightarrow B$ e $g : B \rightarrow C$, si definisce $(g \circ f)(a) = g(f(a))$.

# Proprietà
Una funzione $f : A \rightarrow B$ è:
- iniettiva se $a_1 \neq a_2 \implies f(a_1) \neq f(a_2)$
- surgettiva se $\forall b \in B$   $\exists a \in A$   $b = f(a)$
- bigettiva se iniettiva e surgettiva
- pari se $f(x) = f(-x)$
- dispari se $f(-x) = -f(x)$
- periodica se $\exists p$   $f(x+p) = f(x)$
- monotona se $x > y \implies f(x)$   $\{>, \geq, <, \leq\}$   $f(y)$

# Inverse
Data una funzione $f : A \rightarrow B$, una funzione $g : B \rightarrow A$ è detta:
- inversa sinistra di $f$ se $g \circ f = id$
- inversa destra di $f$ se $f \circ g = id$
- inversa di $f$ se è sia inversa sinistra che destra

Per ogni funzione valgono:
- invertibile a sinistra $\iff$ iniettiva
- invertibile a destra $\iff$ surgettiva

# Funzioni elementari
Potenza: $f_k(x) = x^k$
- pari
- bigettiva su opportuni intervalli $\implies$ invertibile con la radice

Valore assoluto: $f(x) = |x|$
- pari
- vale $|x+y| \leq |x| + |y|$
- vale $||x| - |y|| \leq |x-y|$

Esponenziale: $f_a(x) = a^x$
- strettamente crescente
- bigettiva $\implies$ invertibile col logaritmo
- unica se definita con i seguenti assiomi:
	- $f_a(x+y) = f_a(x)f_a(y)$
	- $f_a(1) = a$
	- non implode in $\mathbb R$

Seno: $f(x) = \sin x$
- dispari
- periodica con periodo minimo $2\pi$
- strettamente crescente e bigettiva su opportuni intervalli $\implies$ invertibile con l'arcoseno

Coseno: $f(x) = \cos x$
- pari
- periodica con periodo minimo $2\pi$
- strettamente decrescente e bigettiva su opportuni intervalli $\implies$ invertibile con l'arcocoseno

Tangente: $f(x) = \tan x$
- dispari
- periodica con periodo minimo $\pi$
- strettamente crescente e bigettiva su opportuni intervalli $\implies$ invertibile con l'arcotangente