# Funzione a più variabili
Sia $f : \mathbb{R}^n \to \mathbb{R}^m$, allora $f$ si dice:
- scalare se $m = 1$
- curva se $n = 1$
- campo vettoriale se $m=n$

Dato $y \in \mathbb{R}^m$ si dice insieme di livello la preimmagine $f^{-1}(\{ y \})\subseteq \mathbb{R}^n$.

Ogni funzione quadratica è riconducibile a una conica dal grafico paraboloide o a sella.

Le funzioni radiali hanno grafico $S_{r}=\left\{  \sum\limits_{k=1}^{n} x_{k}^2=r^2  \right\}$, ossia una sfera di raggio $r$.

# Metrica
Sia $X$ insieme, una distanza o metrica è una funzione $d : X \times X \to \mathbb{R}$ tale che:
1. $d(x,y)\geq 0$
2. $d(x,y) = 0 \iff x = y$
3. $d(x,y) = d(y,x)$
4. $d(x,z) \leq d(x,y) + d(y,z)$

$(X,d)$ è detto spazio metrico.

Siano $(X, d_{1})$ e $(X,d_{2})$ spazi metrici, le metriche si dicono equivalenti se:
- $\exists C,\tilde{C} > 0$   $\forall x,y \in X$   $Cd_{2}(x,y)\leq d_{1}(x,y) \leq \tilde{C}d_{2}(x,y)$.

Sia $(X,d)$ spazio metrico, $\{ x_{n} \}_{n \in \mathbb{N}} \subseteq X$, $\bar{x} \in X$, si dice che $x_{n}$ tende a $x$ e si scrive $x_{n}\to x$ se $d(x_{n},x)\to {0}$.

# Norma
Sia $V$ spazio vettoriale, una norma è una funzione $||\cdot|| : V \times V \to \mathbb{R}$ tale che:
1. $||v|| \geq 0$
2. $||v|| = 0 \iff v = 0$
3. $||\lambda v||=|\lambda| \, ||v||$
4. $||v+w|| \leq ||v|| + ||w||$

$(V, ||\cdot||)$ è detto spazio normato.

In uno spazio normato, una norma induce una metrica $d(v,w) := ||v-w||$.

Siano $(V, ||\cdot||_{1})$ e $(V, ||\cdot||_{2})$ spazi normati, le norme si dicono equivalenti se:
- $\exists C,\tilde{C} > 0$   $\forall v \in V$   $C||v||_{2} \leq ||v||_{1} \leq \tilde{C}||v||_{2}$.

# Prodotto scalare
Sia $V$ spazio vettoriale, un prodotto scalare è una funzione $\langle\cdot, \cdot \rangle : V \times V \to \mathbb{R}$ tale che:
1. $\langle v,v \rangle \geq 0$
2. $\langle v, v \rangle = 0 \iff v = 0$
3. $\langle v, w \rangle = \langle v, w \rangle$
4. $\langle \lambda u + \mu v, w \rangle = \lambda \langle u, w \rangle + \mu \langle v, w \rangle$

$(V, \langle \cdot, \cdot \rangle)$ è detto spazio euclideo.

In uno spazio euclideo, un prodotto scalare induce una norma $||v|| := \sqrt{ \langle v, v \rangle }$ e una distanza come prima, dette euclidee.

In uno spazio euclideo valgono Young e Cauchy - Schwarz.

# Topologia degli spazi metrici
Sia $(X, d)$ spazio metrico, allora $A \subseteq X$ si dice:
- aperto se $\forall x \in A$   $\exists r > 0$   $B_{r}(x)\subseteq A$
- chiuso se $X \setminus A$ aperto

Il linguaggio topologico di Analisi 1 si estende agli spazi metrici con le palle.