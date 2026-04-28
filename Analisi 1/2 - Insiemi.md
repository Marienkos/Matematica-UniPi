# Insiemi
Gli insiemi possono essere presentati:
- per elenco: A = {2, 4, 6, ...}
- per proprietà: A = {n : "n è un numero pari"}

Le operazioni possibili sono: unione, intersezione, differenza, prodotto cartesiano.

# Numeri reali
Unica quaterna $(\mathbb R, +, *, \geq)$ a meno di isomorfismi, dove $\mathbb R$ è un insieme coi seguenti tipi di assiomi: algebrici, ordinamento, continuità.

Algebricamente $(\mathbb R, +, *)$ è un campo con almeno due elementi.

$\geq$ è un ordinamento totale, gode cioè di totalità, riflessività, transitività e antisimmetricità. Inoltre somma e prodotto positivo non alterano il verso.

Dati $A \subseteq \mathbb R$ e $B \subseteq \mathbb R$ non vuoti, A sta a sinistra di B se $\forall a \in A \; \forall b \in B \; a \leq b$

In tal caso $\exists c \in \mathbb R \; a \leq c \; \forall a \in A \; \land c \leq b \; \forall b \in B$

# Maggioranti e minoranti
Un maggiorante di A è maggiore di ogni elemento di A.

Un maggiorante è detto massimo se appartiene ad A.

L'estremo superiore di A è $+\infty$ se non esistono maggioranti, altrimenti è il minimo maggiorante.

# Esistenza di inf e sup
TESI: In sottoinsiemi reali A inf e sup esistono sempre.

DIMOSTRAZIONE
- Se non ci sono maggioranti, allora il sup esiste.
- Se ci sono maggioranti, chiamiamo B il loro insieme. B sta a destra di A, dunque per l'assioma di continuità esiste un c minimo di B, ossia il sup di A.