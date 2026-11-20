# Proprietà T
$X$ topologico si dice:
- $T_{0}$ se $\forall x\neq y \in X$   $(\exists U \in I(x)$   $y \not\in U) \lor (\exists V \in I(y)$   $x \not\in V)$
- $T_{1}$ se $\forall x \neq y \in X$   $\exists U \in I(x),V \in I(y)$   $x \not\in V \land y \not\in U$
- $T_{2}$ se $\forall x \neq y \in X$   $\exists U \in I(x),V \in I(y)$   $U \cap V = \emptyset$

$T_{2} \implies T_{1} \implies T_{0}$.

Sono equivalenti:
1. $X$ $T_{1}$
2. Tutti i singoletti $\{ x \} \subseteq X$ sono chiusi
3. La topologia di $X$ è più fine della topologia cofinita

DIMOSTRAZIONE:
- (1.) $\implies$ (2.)
	1. Siano $\{ x \}$ singoletto e $y \in X \setminus \{ x \}$, per $T_{1}$ si trova $V \in I(y)$   $x \not\in V$
	2. $V \subseteq X \setminus \{ x \}$, da cui $X \setminus \{ x \} \in I(y)$ e $X \setminus \{ x \}$ è aperto
- (2.) $\implies \bigcup\limits_{i = 1}^n \{ x_{i} \}$ chiuso $\implies$ (3.)
- (3.) $\implies$ (1.) con $U = X \setminus \{ y \}$ e $V = X \setminus \{ x \}$

$X$ infinito con topologia cofinita $\implies X$ $T_{1}$ ma non $T_{2}$.

Siano $X$ $T_{2}$ e $\{ x_{n} \} \subseteq X$, allora $x_{n} \to \bar{x}\land x_{n} \to \bar{y} \implies \bar{x} = \bar{y}$.

DIMOSTRAZIONE: