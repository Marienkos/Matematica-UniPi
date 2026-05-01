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