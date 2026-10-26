# Conica proiettiva
Sia da ora in poi $\mathbb{K}$ campo di caratteristica non 2.

Sia $\mathbb{K}[x_{0},x_{1},x_{2}]_{2} = \{ \text{monomi di grado totale }2 \} \cup \{ 0 \}$.

$\mathbb{K}[x_{0},x_{1},x_{2}]$ spazio vettoriale di base $x_{0}^2,x_{1}^2,x_{2}^2,x_{0}x_{1},x_{0}x_{2},x_{1}x_{2}$ dunque di dimensione 6.

Una conica proiettiva su $\mathbb{K}$ è un elemento di $\mathbb{P}(\mathbb{K}[x_{0},x_{1},x_{2}]_{2})$.

Se $C = [p]$ è una conica, il suo supporto è $V(C)=\{ [x_{0},x_{1},x_{2}] \in \mathbb{P}^2(\mathbb{K}) : p(x_{0},x_{1},x_{2})=0 \}$.

Se $\mathbb{K} = \mathbb{C}$, allora $C = C' \iff V(C) = V(C')$.

Sia $f : \mathbb{P}^2(\mathbb{K}) \to \mathbb{P}^2(\mathbb{K})$ proiettività con $f = [\varphi]$ e $C = [p]$ conica, allora l'immagine di $C$ tramite $f$ è $f(C) = [p \circ \varphi^{-1}]$.

$V(f(C))=f(V(C)) \subseteq \mathbb{P}^2(\mathbb{K})$.

DIMOSTRAZIONE:
1. Sia $Q \in \mathbb{P}^2(\mathbb{K})$ con $Q = [v]$ e $Q \in V(f(C))$
2. $(p \circ \varphi^{-1})(v)=0 \iff[\varphi^{-1}(v)] \in V(C) \iff f^{-1}(Q) \in V(C) \iff Q \in f(V(C))$

# Classificazione
Due coniche $C$ e $C'$ si dicono proiettivamente equivalenti se $\exists f$ proiettività   $C' = f(C)$.

Dato $p(x_{0},x_{1},x_{2}) = {}^txAx$, si dice che la matrice $A$ rappresenta $C = [p]$ e si denota con $C = [A]$.

Dato $p$ si ha una sola matrice e viceversa.

Data $f : \mathbb{P}^2(\mathbb{K}) \to \mathbb{P}^2(\mathbb{K})$ proiettività rappresentata da $M$, vale $f(C)$ rappresentata da $p \circ M^{-1}$.

Se $A$ rappresenta $C$, allora ${}^tM^{-1}AM^{-1}$ rappresenta $f(C)$.

La relazione $A \sim A' \iff \exists \lambda \in \mathbb{K}^*$   $\exists M \in \text{GL}_{3}(\mathbb{K})$   $A' = \lambda \cdot {}^tMAM$ è d'equivalenza.

Siano $C = [A]$ e $C' = [A']$ due coniche, allora $C$ proiettivamente equivalente a $C' \iff A \sim A'$.

Se $\mathbb{K} = \mathbb{C}$, il rango è un invariante completo e ci sono 3 classi di equivalenza.

Se $\mathbb{K} = \mathbb{R}$, le matrici simmetriche a meno di congruenza sono classificate dalla segnatura.

# Parte affine
Data $C$ conica, la parte affine di $C$ è la conica affine di $\mathbb{K}^2$ di equazione $f(x,y)=p(1,x,y)$.

Il supporto della parte affine di $C$ è $V(C) \cap U_{0}$.

DIMOSTRAZIONE: $(x,y)$ nel supporto $\iff f(x,y) = 0 \iff p(1,x,y) = 0 \iff [1,x,y] \in V(C)$.

# Chiusura proiettiva
La chiusura proiettiva $\overline{C}$ di una conica affine $C$ è $\overline{C} = [p]$ con $p(x_{0},x_{1},x_{2}) = x_{0}^2f\left( \frac{x_{1}}{x_{0}}, \frac{x_{2}}{x_{0}} \right)$.

Se $C = [A]$, anche $\overline{C} = [A]$.

$C$ si classifica come:
- ellisse se $V(\overline{C}) \cap H_{0} = \emptyset$
- parabola se $|V(\overline C) \cap H_{0}| = 1$
- iperbole se $|V(\overline C) \cap H_{0}| = 2$

DIMOSTRAZIONE:
1. Si mette a sistema con $x_{0} = 0$
2. Si guardano le intersezioni con $H_{0}$
3. Esse sono determinate da un sistema $2\times 2$
4. Si guarda la matrice dei coefficienti $\tilde{A}$

# Intersezioni tra coniche e rette
Siano $C = [p]$ conica di $\mathbb{P}^2(\mathbb{K})$ e $r \subseteq \mathbb{P}^2(\mathbb{K})$ retta di equazione $f(x_{0},x_{1},x_{2})=0$. Allora $r$ è una componente di $C$ se $f \mid p$.

Se $r$ è una componente di $C$, allora $r \subseteq V(C)$.

$C$ si dice riducibile se ha una retta come componente.

$C$ riducibile $\iff p$ riducibile.

Sia $f$ proiettività, allora $r$ componente di $C \iff f(r)$ componente di $f(C)$.

Se $|r \cap V(C)|\geq 3$, allora $r$ componente di $C$.

DIMOSTRAZIONE:
1. Siano $Q = [v]$ e $R = [w]$ punti distinti su $r$
2. $r$ è parametrizzata da $[\lambda,\mu] \mapsto [\lambda v + \mu w]$
3. I punti di $r \cap V(C)$ sono soluzioni omogenee di $G(\lambda,\mu) = p(\lambda v + \mu w) = 0$
4. Se $G(\lambda,\mu) \equiv 0$, allora $r$ è componente di $C$
5. Se $G(\lambda,\mu)$ non è nullo, allora $|r \cap V(C)| \leq 2$

$C$ riducibile $\implies C$ degenere.

DIMOSTRAZIONE:
1. $C = [p]$ riducibile $\implies p$ prodotto di due fattori lineari omogenei
2. I due fattori si possono scrivere come ${}^tvx = 0$ e ${}^twx=0$ con $v,w\neq 0$
3. $p(x_{0},x_{1},x_{2}) = ({}^tvx)({}^twx)={}^t({}^tvx)({}^twx)={}^txv\cdot{}^twx = {}^tx\left( \frac{v^tw+w^tv}{2} \right)x$
4. I ranghi a numeratore sono $\leq 1$, quindi il rango della matrice è $\leq 2$ e $C$ degenere

Se $\mathbb{K} = \mathbb{C}$ vale  $C$ degenere $\implies C$ riducibile.

DIMOSTRAZIONE: $\mathbb{K} = \mathbb{C}$ e $C$ degenere $\implies C$ proiettivamente equivalente a $x_{0}^2$ o $x_{0}^2 + x_{1}^2$.

$r \subseteq V(C) \implies r$ componente di $C$

# Retta tangente
Siano $C$ conica non degenere e $Q \subseteq V(C)$. Una retta $r \subseteq \mathbb{P}^2(\mathbb{K})$ si dice tangente a $C$ nel punto $Q$ se $r \cap V(C) = \{ Q \}$.

Si dice molteplicità di intersezione la molteplicità della radice $[\lambda_{i},\mu_{i}]$ corrispondente a $Q$ nell'equazione $G(\lambda,\mu)$.

Siano $C$ conica e $Q \subseteq V(C)$. Una curva $\gamma \subseteq \mathbb{P}^n(\mathbb{K})$ si dice tangente a $C$ nel punto $Q$ se la molteplicità di intersezione di $Q$ è $\geq 2$.

Siano $C \subseteq \mathbb{P}^2(\mathbb{K})$ conica non degenere e $Q \subseteq V(C)$. Allora:
1. $\exists! \tau_{Q}$ retta passante per $Q$ tangente a $C$ in $Q$
2. $C = [M]$ con $M$ matrice simmetrica $3 \times 3$ e $Q = [v] \implies \tau_{Q}$ ha equazione ${}^tvMx=0$

DIMOSTRAZIONE:
1. Si fissa $r$ passante per $Q$, sia $[w] \in r$ distinto da $Q$
2. Si parametrizza $r$ tramite $[\lambda,\mu] \mapsto [\lambda v + \mu w]$
3. $Q \mapsto [1,0]$ e $G(\lambda,\mu) = p(\lambda v+\mu w) = {}^t(\lambda v+\mu w)M(\lambda v+\mu w)=\mu(2\lambda^tvMw+\mu^twMw)$
4. $r$ tangente a $C$ in $Q \iff$ unico $[\lambda,\mu]$ che la soddisfa è $[1,0] \iff {}^tvMw=0$
5. La retta per $Q$ e $[w]$ è tangente a $C \iff {}^tvMw=0$
6. La retta di equazione ${}^tvMw=0$ è tangente a $C$ ed è l'unica

# Polarità
Siano $C \subseteq \mathbb{P}^2(\mathbb{K})$ conica non degenere, $V(C)=[M]$ con $M$ matrice simmetrica $3\times 3$ e $P = [v] \in \mathbb{P}^2(\mathbb{K})$. La retta polare di $P$ rispetto a $C$ è la retta di $\mathbb{P}^2(\mathbb{K})$ di equazione ${}^t(Mv)x=0$ e si denota con $\text{pol}_{C}(P)$.

$\text{pol}_{C} : \mathbb{P}^2(\mathbb{K}) \to \mathbb{P}^2(\mathbb{K})^*$ è la trasformazione proiettiva rappresentata da $M$ in coordinate ovvie.

Valgono:
1. $P \in V(C) \implies\text{pol}_{C}(P) = \tau_{Q}$ tangente a $C$ in $P$
2. $P \in \text{pol}_{C}(Q) \iff Q \in \text{pol}_{C}(P)$
3. $\text{pol}_{C}(P) \cap V(C) = \{ Q \in V(C) : P \in \tau_{Q}\}$
4. $P \in \text{pol}_{C}(P) \implies P \in V(C)$
5. $|\text{pol}_{C}(P) \cap V(C)|=1 \implies P \in V(C)$

DIMOSTRAZIONE:
1. Teorema precedente
2. Se $P = [v]$ e $Q = [w]$, allora $P \in \text{pol}(Q) \iff {}^twMv=0 \iff  {}^tvMw = 0 \iff Q \in \text{pol}(P)$
3. $Q \in \text{pol}(P) \cap V(C) \iff P \in \text{pol}(Q) \land Q \in V(C) \iff P \in \tau_{Q} \land Q \in V(C)$
4. $\text{pol}(P)$ ha equazione ${}^tvMx=0$, da cui $P \in \text{pol}(P) \implies {}^tvMv=0 \implies P \in V(C)$
5. $Q = \text{pol}(P) \cap V(C) \implies \text{pol}(Q) = \tau_{Q} = \text{pol}(P)$ e per costruzione $P=Q \in V(C)$

# Conica duale
Sia $C \subseteq \mathbb{P}^2(\mathbb{K})$ conica non degenere, si dice conica duale $C^* := \text{pol}(C)$.

I punti di $V(C^*)$ sono le rette tangenti $\{ \tau_{Q} : Q \in V(C) \}$ viste come punti di $\mathbb{P}^2(\mathbb{K})^*$.

Se $C = [M]$, allora $C^* = [M^{-1}]$.

DIMOSTRAZIONE: Nelle coordinate standard $\text{pol} = [M]$ e $C^* = \text{pol}(C) =[{}^tM^{-1}MM^{-1}]=[M^{-1}]$.

Ogni conica non degenere in $\mathbb{P}^2(\mathbb{K})$ è duale di un'unica conica.

DIMOSTRAZIONE: $C = [M] \implies C^* = [M^{-1}]$ ha come conica duale $C$.

DIMOSTRAZIONE: Esiste l'isomorfismo naturale $\mathbb{P}^2(\mathbb{K}) \cong \mathbb{P}^2(\mathbb{K})^{**}$ da cui $C = C^{* *}$.