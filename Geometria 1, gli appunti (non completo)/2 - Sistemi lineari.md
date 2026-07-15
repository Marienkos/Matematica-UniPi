# Matrice
Una matrice $m\times n$ in $\mathbb{K}$ è una griglia di $m$ righe e $n$ colonne a valori in $\mathbb{K}$.

Dati un vettore riga $\underline{x}$ e un vettore colonna $\underline{y}$, il prodotto è $\sum\limits_{i=1}^{n} x_{i}y_{i}$.

Date due matrici $A$ e $B$, il prodotto è $M$ tale che $M_{i,j}=A_{i}B^j$.

L'insieme delle matrici $\mathscr{M}_{m,n}(\mathbb{K})$ è uno spazio vettoriale.

Una matrice $A$ è invertibile se $\exists A^{-1}$, detta inversa, tale che $AA^{-1}=I = A^{-1}A$.

Date due matrici $A,B \in \mathscr{M}_{m,n}(\mathbb{K})$ invertibili, $AB$ è invertibile e $(AB)^{-1}=B^{-1}A^{-1}$.

Le matrici invertibili di $\mathscr{M}_{n}(\mathbb{K})$ formano un gruppo denotato con $\text{GL}_{n}(\mathbb{K})$.

L'applicazione $f_{A} : \mathbb{K}^n \to \mathbb{K}^n$ data da $\underline{x} \mapsto A\underline{x}$ è lineare.

# Sistema lineare
Dato un sistema di $m$ equazioni in $n$ variabili, si può ricondurre alla forma $A\underline{x} = \underline{b}$, dove:
1. $A\in \mathscr{M}_{m,n}(\mathbb{K})$ è la matrice dei coefficienti delle variabili
2. $\underline{x}$ è il vettore delle variabili
3. $\underline{b}$ è il vettore dei termini noti

Sia $f : V \to W$ lineare. Si definiscono i sottospazi vettoriali:
- nucleo di $f$, ossia l'insieme $\text{Ker}f = \{ \underline{v} \in V : f(\underline{v})=\underline{0} \}$
- immagine di $f$, ossia l'insieme $\mathrm{Im}f=f(V)$

Se il sistema è omogeneo, ossia nella forma $A\underline{x}=\underline{0}$, le soluzioni sono $\underline{x} \in \text{Ker}f_{A}$.

Se il sistema non è omogeneo, allora $A\underline{x}=\underline{b}$ risolubile $\iff b \in \mathrm{Im}f_{A}=\text{Span}(A^1,\dots,A^n)$.
 
Sia $f : V \to W$ lineare. Allora $f$ iniettiva $\iff \text{Ker}f = \{ \underline{0} \}$.

# Rango
Si dice rango di $A$ il numero $\text{rg}A =\dim\text{Span}(A^1,\dots,A^n)=\dim (\mathrm{Im}f_{A})$.

Sia $f : V \to W$ lineare. Allora $\dim V = \dim(\text{Ker}f) + \dim(\mathrm{Im}f)$.

DIMOSTRAZIONE:
1. Sia $\underline{v}_{1},\dots,\underline{v}_{k}$ base di $\text{Ker}f$ estesa a $\underline{v}_{1},\dots,\underline{v}_{n}$ base di $V$
2. Siano $\underline{w}_{k+1}=f(\underline{v}_{k+1}),\dots,\underline{w}_{n}$
3. Essi sono linearmente indipendenti e generano $\mathrm{Im}f$

$\text{dim}\{ \underline{x} : A\underline{x} = \underline{0} \}=n-\text{rg}A$.

DIMOSTRAZIONE: $\dim\{ \underline{x} : A\underline{x} = \underline{0} \} = \dim\text{Ker}f_{A}= \dim\mathbb{K}^n-\dim\mathrm{Im} f_{A} = n -\text{rg}A$.

# Teorema di Rouché - Capelli
Sia $A\underline{x}=\underline{b}$ lineare e $\tilde{A} = [A|\underline{b}]$ la matrice completa. Allora $A\underline{x}=\underline{b}$ risolvibile $\iff\text{rg}A =\text{rg} \tilde{A}$.

DIMOSTRAZIONE: $A\underline{x}=\underline{b}$ risolvibile $\iff b \in \mathrm{Im} f_{A} \iff\text{rg}A =\text{rg}\tilde{A}$.

# Matrice a scala
Le soluzioni di un sistema sono invariate per le seguenti operazioni di Gauss su $\tilde{A}$:
1. Scambio di righe
2. Moltiplicazione di una riga per un numero $\neq 0$
3. Somma del multiplo di una riga a un'altra riga

DIMOSTRAZIONE:
1. L'ordine delle equazioni in un sistema non conta
2. $a_{i_{1}}x_{1}+\dots+a_{i_{n}}x_{n}=b_{i} \iff \lambda a_{i_{1}}x_{1}+\dots+\lambda a_{i_{n}}x_{n} = \lambda b_{i}$ con $\lambda\neq 0$
3. Ragionamenti sulle soluzioni

Le operazioni di Gauss non cambiano lo span delle righe.

DIMOSTRAZIONE:
1. L'ordine delle righe non modifica lo span
2. $\text{Span}(\underline{v}_{1},\dots,\underline{v}_{i},\dots,\underline{v}_{n}) =\text{Span}(\underline{v}_{1},\dots \lambda \underline{v}_{i},\dots,\underline{v}_{n})$ con $\lambda\neq 0$
3. $\text{Span}(\underline{v}_{1},\dots,\underline{v}_{i},\dots,\underline{v}_{n}) =\text{Span}(\underline{v}_{1},\dots \underline{v}_{i}+\lambda \underline{v}_{j},\dots,\underline{v}_{n})$ con $i\neq j$

Una matrice $A$ si dice a scala se $\forall A_{i}=[0,\dots,0, A_{i,j}=\text{pivot}, \dots]$   $\forall m\geq i$   $\forall n \leq j$   $A_{m,n}=0$.

Ogni matrice può essere ridotta a scala tramite operazioni di Gauss.

$k$ vettori a scala sono linearmente indipendenti.

DIMOSTRAZIONE: La combinazione nulla è unica risalendo per le righe.

Sia $A$ una matrice e $S$ la sua ridotta a scala. Allora $\text{rg}S = k$.

DIMOSTRAZIONE:
1. Le colonne dei pivot sono linearmente indipendenti per il lemma precedente
2. Sia $W_{k}=\{ \underline{y} \in \mathbb{K}^m : y_{i}= 0\text{ per }i>k \} =\text{Span}\{ e_{1},\dots,e_{n} \}$
3. Poiché $\dim W_{k} = k$ le colonne dei pivot sono base

$\text{rg}A =\text{rg}S$.

DIMOSTRAZIONE: Le soluzioni del sistema omogeneo associato non cambiano.

Si dice rango per righe $\tilde{\text{rg}}A = \dim\text{Span}(A_{1},\dots,A_{n})$

$\forall A \in \mathscr{M}_{m,n}(\mathbb{K})$   $\text{rg}A=\text{rg}S=\tilde{\text{rg}}A$.

DIMOSTRAZIONE: Ovvio per matrici a scala e lo span delle righe non cambia riducendo.

Dalle proposizioni precedenti discendono:
1. $\text{rg}A$ può assumere tutti i valori tra $0$ e $\min\{ m,n \}$
2. $\text{rg}A =\text{rg}{}^t{A}$

Una ridotta a scala di $A$ si trova moltiplicando $A$ a sinistra per una matrice invertibile.

# SD-equivalenza
Due matrici $A,B \in \mathscr{M}_{m,n}(\mathbb{K})$ si dicono S-equivalenti o equivalenti a sinistra e si denotano con $A \sim_{S}B$ se $\exists P \in\text{GL}_{m}(\mathbb{K})$   $B = PA$.

$P \in\text{GL}_{n}(\mathbb{K}) \implies\text{rg}P = n$.

Due matrici $A,B \in \mathscr{M}_{m,n}(\mathbb{K})$ si dicono D-equivalenti o equivalenti a destra e si denotano con $A \sim_{D} B$ se $\exists Q \in\text{GL}_{m}(\mathbb{K})$   $B = AQ$.

Due matrici $A,B \in \mathscr{M}_{m,n}(\mathbb{K})$ si dicono SD-equivalenti e si denotano con $A\sim_{SD} B$ se $\exists P \in\text{GL}_{n}(\mathbb{K})$ ed $\exists Q \in\text{GL}_{m}(\mathbb{K})$   $B = PAQ$.

$A \sim_{SD} B \iff B$ si ottiene da $A$ tramite operazioni di Gauss di riga e colonna.

$A \sim_{SD} B \iff\text{rg}A=\text{rg}B$.

DIMOSTRAZIONE: La relazione è equivalente a ridurre a scala per righe e colonne.

