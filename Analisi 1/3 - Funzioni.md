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