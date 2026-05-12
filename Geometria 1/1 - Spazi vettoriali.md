# Spazio vettoriale
Sia $V$ un gruppo abeliano rispetto alla somma e $\mathbb{K}$ un campo. $V$ si dice spazio vettoriale su $\mathbb{K}$ se:
1. $\alpha(\underline{v}+\underline{w}) = \alpha \underline{v} + \alpha \underline{w}$   $\forall \alpha \in \mathbb{K}$   $\forall \underline{v},\underline{w} \in V$
2. $(\alpha+\beta)\underline{v} = \alpha \underline{v} + \beta \underline{v}$   $\forall \alpha,\beta \in \mathbb{K}$   $\forall \underline{v} \in V$
3. $\alpha(\beta \underline{v}) = (\alpha\beta) \underline{v}$   $\forall\alpha,\beta \in \mathbb{K}$   $\forall \underline{v} \in V$
4. $1\underline{v} = \underline{v}$

Gli elementi di uno spazio vettoriale sono detti vettori.

Sia $V$ spazio vettoriale su $\mathbb{K}$. Un sottoinsieme $W \subseteq V$ non vuoto si dice sottospazio vettoriale se chiuso rispetto a somma e prodotto esterno.

Siano $U,W \subseteq V$ sottospazi vettoriali. Allora $U \cap W$ sottospazio vettoriale

# Combinazione lineare
Dati $\underline{v}_{1},\dots,\underline{v}_{n} \in V$, si dice combinazione lineare $\sum\limits_{i=1}^{n} \alpha_{i}\underline{v}_{i}$ con $\alpha_{i}\in \mathbb{K}$.

Si definisce $\text{Span}(\underline{v}_{1},\dots,\underline{v}_{n})=\{ \text{combinazioni lineari} \}$.

Lo Span è un sottospazio vettoriale di $V$. Più in generale, dato $A \subseteq V$, $\text{Span(A)}$ ssp vettoriale di $V$.

DIMOSTRAZIONE: Verifica gli assiomi.

Un insieme $A \subseteq V$ si dice insieme di generatori di $V$ se $\text{Span}(A)=V$.

I vettori $\underline{v}_{1},\dots,\underline{v}_{n}\in V$ si dicono linearmente indipendenti se $\sum\limits_{i=1}^{n} \alpha_{i}\underline{v}_{i}=0 \iff \alpha_{1}=\dots=\alpha_{n}=0$.

Se $\underline{v}_{1},\dots,\underline{v}_{n}$ sono linearmente indipendenti, allora $\underline{v} = \sum\limits_{i=0}^{n} \alpha_{i}\underline{v}_{i}=\sum\limits_{i=0}^{n} \beta_{i}\underline{v}_{i} \implies \alpha_{i}=\beta_{i}$   $\forall\alpha_{i},\beta_{i} \in \mathbb{K}$.

# Base e coordinate
Una base $\mathscr{B} \in V$ è un sottoinsieme di generatori linearmente indipendente.

Ogni vettore $\underline{v} \in V$ si scrive in modo unico come combinazione lineare dei vettori di $\mathscr{B}$, i coefficienti sono detti coordinate di $\underline{v}$ rispetto a $\mathscr{B}$ e si indica con $[\underline{v}]_{\mathscr{B}} \in \mathbb{K}^n$.

L'applicazione $\varphi_{\mathscr{B}} : V \to \mathbb{K}^n$ data da $\underline{v}\mapsto[\underline{v}]_{\mathscr{B}}$ è una bigezione tale che:
1. $[v+w]_{\mathscr{B}} = [\underline{v}]_{\mathscr{B}} + [\underline{w}]_{\mathscr{B}}$
2. $[\alpha \underline{v}]_{\mathscr{B}}=\alpha[\underline{v}]_{\mathscr{B}}$

DIMOSTRAZIONE: Combinazioni lineari.

Una base è un insieme:
- linearmente indipendente massimale, ossia $B \supsetneq A$ non è linearmente indipendente
- di generatori minimale, ossia $B \subsetneq A$ non genera $V$

DIMOSTRAZIONE: Definizioni.

Ogni spazio vettoriale ha una base.

DIMOSTRAZIONE: Proposizione precedente.

Due basi $\mathscr{B}$ e $\mathscr{B}'$ di $V$ hanno lo stesso numero di elementi, detto dimensione di $V$.

DIMOSTRAZIONE: Si può passare da una base all'altra tramite algoritmo di scambio.

# Somma di spazi
Si definisce $U+W = \{ \underline{u} + \underline{w} : u \in U, w \in W \}$. Allora $U + W = \text{Span}(U \cup W)$ sottospazio vettoriale.

DIMOSTRAZIONE: $\underline{v} \in \text{Span}(U \cup W) \iff \underline{v} = \alpha \underline{u} + \beta \underline{w} \iff \underline{v} \in U+W$.

Due sottospazi $U$ e $W$ si dicono in somma diretta se $U \cap W = \{ \underline{0} \}$ e si denota con $U \oplus W$.

Sia $Z = U + W$. Allora $Z = U \oplus W \iff \forall \underline{z} \in Z$   $\exists!\underline{u}\in U$   $\exists!\underline{w}\in W$   $\underline{z}=\underline{u}+\underline{w}$.

DIMOSTRAZIONE:
- ($\implies$) $\underline{z} = \underline{u}+\underline{w} = \underline{u}'+\underline{w}' \implies \underline{v} = \underline{u}-\underline{u}' = \underline{w}-\underline{w}' \in U \cap W = \{ \underline{0} \} \implies \underline{v} = \underline{0}$
- ($\impliedby$) $\underline{v} = \underline{v} + \underline{0} = \underline{0} + \underline{v} \in U \cap W$

Sia $W \subseteq V$ sottospazio vettoriale. Si dice supplementare di $W$ un ssp $U$ tale che $V = U \oplus W$.

# Formula di Grassmann
Siano $U,W\subseteq V$ sottospazi vettoriali. Allora $\dim(U+W)=\dim U + \dim W - \dim(U \cap W)$.

DIMOSTRAZIONE:
1. Sia $\mathscr{B}_{1}$ base di $U \cap W$. La estendo a $\mathscr{B}_{2}$ base di $U$ e $\mathscr{B}_{3}$ base di $W$
2. $\mathscr{B} = \mathscr{B}_{2} \cup \mathscr{B}_{3}$ base di $U+W$ $\implies$ tesi