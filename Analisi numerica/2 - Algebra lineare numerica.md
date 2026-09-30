# Teoremi di Gershgorin
Sia $A \in \mathbb{C}^{n\times n}$ e $\lambda$ un suo autovalore. Se $x_{h}$ è una coordinata di modulo massimo di un autovettore $v$ relativo a $\lambda$, allora $\lambda \in K_{h}$.

DIMOSTRAZIONE: Si pone $Av = \lambda v$ e si sostituiscono i prodotti tra matrici.

Se esistono famiglie di cerchi Gershgorin disgiunte, l'unione dei cerchi di ogni famiglia contiene esattamente tanti autovalori quanti i cerchi nella famiglia.

DIMOSTRAZIONE:
1. Si pone $A(t)=D + t(A - D)$
2. $A(0)=D$ e $A(1) = A$
3. $A(t)$ continuo in $t$
4. Gli autovalori di $A(t)$ al variare di $t$ non possono uscire dai cerchi di Gershgorin

Una matrice si dice irriducibile se non esiste una base nella quale è triangolare a blocchi.

$A$ irriducibile $\iff$ grafo associato ad $A$ fortemente connesso.

DIMOSTRAZIONE: Permutazioni e grafi.

Sia $\lambda$ un autovalore di $A$ tale che $\lambda \in K_{i} \implies \lambda \in \partial K_{i}$. Allora $A$ irriducibile $\implies \lambda \in \bigcap\limits_{i \in I} \partial K_{i}$.

DIMOSTRAZIONE: Teorema precedente.

Gli ovali di Cassini sono delle estensioni più forti dei cerchi di Gershgorin.

# Forma normale di Schur
$\forall A\in \mathbb{C}^{n\times n}$   $\exists T$ triangolare superiore   $\exists U$ unitaria   $U^H AU = T$.

DIMOSTRAZIONE: Induzione sulla taglia di $A$.

$T \in \mathbb{R}^{n\times n}$ si dice quasi triangolare se è triangolare con numeri reali o blocchi $2\times 2$ con coppie di autovalori complessi coniugati.

$\forall A \in \mathbb{R}^{n\times n}$   $\exists T$ quasi triangolare superiore   $\exists Q$ ortogonale   $Q^T A Q = T$.g 