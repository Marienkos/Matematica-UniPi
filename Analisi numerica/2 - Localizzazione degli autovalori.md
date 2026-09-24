# Teoremi di Gershgorin
Sia $A \in \mathbb{C}^{n\times n}$ e $\lambda$ un suo autovalore. Se $x_{h}$ è una coordinata di modulo massimo di un autovettore $v$ relativo a $\lambda$, allora $\lambda \in K_{h}$.

DIMOSTRAZIONE: Si pone $Av = \lambda v$ e si sostituiscono i prodotti.

Se esistono famiglie di cerchi Gershgorin disgiunte, l'unione dei cerchi di ogni famiglia contiene esattamente tanti autovalori quanti i cerchi nella famiglia.

DIMOSTRAZIONE:
1. Si pone $A(t)=D + t(A - D)$
2. $A(0)=D$ e $A(1) = A$
3. $A(t)$ continuo in $t$
4. Gli autovalori di $A(t)$ al variare di $t$ non possono uscire dai cerchi di Gershgorin