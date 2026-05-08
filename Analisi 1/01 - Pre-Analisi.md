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

# Numeri reali
Unica quaterna $(\mathbb R, +, *, \geq)$ a meno di isomorfismi, dove $\mathbb R$ è un insieme coi seguenti tipi di assiomi: algebrici, ordinamento, continuità.

Algebricamente $(\mathbb R, +, *)$ è un campo con almeno due elementi.

$\geq$ è un ordinamento totale, gode cioè di totalità, riflessività, transitività e antisimmetricità. Inoltre somma e prodotto positivo non alterano il verso.

Dati $A \subseteq \mathbb R$ e $B \subseteq \mathbb R$ non vuoti, A sta a sinistra di B se $\forall a \in A$   $\forall b \in B$   $a \leq b$

In tal caso $\exists c \in \mathbb R$   $a \leq c$   $\forall a \in A$   $\land c \leq b$   $\forall b \in B$

In $\mathbb{R}$ sono detti insiemi connessi e/o convessi $\emptyset$, i punti, gli intervalli con o senza estremi, le semirette e $\mathbb{R}$ stesso.

# Maggioranti e minoranti
Un maggiorante di A è maggiore di ogni elemento di A. Al contrario per il minorante.

Un maggiorante è detto massimo se appartiene ad A. Il minorante è detto minimo.

L'estremo superiore di A, anche detto $\sup A$, è $+\infty$ se non esistono maggioranti, altrimenti è il minimo maggiorante. Al contrario per l'estremo inferiore, anche detto $\inf A$.

# Esistenza di inf e sup
In sottoinsiemi reali A inf e sup esistono sempre.

DIMOSTRAZIONE
- Se non ci sono maggioranti, allora il sup esiste.
- Se ci sono maggioranti, chiamiamo B il loro insieme. B sta a destra di A, dunque per l'assioma di continuità esiste un c minimo di B, ossia il sup di A.

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