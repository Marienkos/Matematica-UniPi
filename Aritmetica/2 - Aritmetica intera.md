# Teorema della divisione euclidea
Dati $a \in \mathbb{Z}$ e $b \in \mathbb{Z}^+$ è possibile la loro divisone euclidea, ossia in $\mathbb{Z}$ esistono e sono unici $q$ quoziente e $r$ resto tali che $a = bq+r$ con $0 \leq r < b$.

DIMOSTRAZIONE:
1. Wlog $a \geq 0$
2. Per principio del minimo $Q = \{ m \in \mathbb{N} : mb \geq a \} \neq \emptyset$ ammette minimo $q$
3. Se $qb=a$ si ha la divisione euclidea $a = qb + 0$
4. Se $qb > a$ si ha $(q-1)b>a$ e $r = a-(q-1)b$ soddisfa l'ipotesi, da cui $a = (q-1)b+r$

# Massimo comun divisore
Siano $a,b \in \mathbb{Z}$ con $a \neq 0 \lor b \neq 0$. Allora il loro massimo comun divisore è l'unico $d \in \mathbb{Z}^+$ tale che:
1. $d | a \land d | b$
2. $c | a \land c | b \implies c \leq d$

Il massimo comun divisore di $a$ e $b$ è denotato con $\text{MCD}(a,b)$ o $(a,b)$ in base al contesto.

La definizione è ben posta.

DIMOSTRAZIONE: Per principio del minimo esiste sempre l'MCD ed è unico.

Valgono:
- $(a,b) = (b,a) = (|a|, |b|)$
- $(a,a) = (a,0) = |a|$

Dati $a,b,c,d \in \mathbb{Z}$ con uno tra $a$ e $b$ e uno fra $b$ e $d$ non nulli, se $a = bc + d$ allora $(a,b) = (b,d)$.

DIMOSTRAZIONE: $\gamma | a \land \gamma | b \implies \gamma | a-bc = d$ e viceversa.

Per calcolare $(a,b)$ si usa l'algoritmo di Euclide:
1. Sia $|a| = |b|q + r_{1}$ euclidea
2. Sia $|b| = r_{1}q_{1} + r_{2}$ euclidea
3. Continui così fino a $r_{n-1}=r_{n}q_{n}$
4. $(a,b) = (|a|,|b|) = r_{n}$

DIMOSTRAZIONE: Induzione sul numero di passi.

# Lemma di Bézout
Dati $a,b \in \mathbb{Z}$ con $a \neq 0 \lor b \neq 0$ esistono $m,n \in \mathbb{Z}$ tali che $(a,b) = am + bn$.

DIMOSTRAZIONE:
1. Sia $\text{CL}^+(a,b) = \{ ar+bs : r \in \mathbb{Z}, s \in \mathbb{Z}, ar+bs>0 \}$
2. $\text{CL}^+(a,b) \neq \emptyset$ e $\text{CL}^+(a,b) \subseteq \mathbb{N}$, per cui ammette minimo $d$
3. $d \in \text{CL}^+(a,b) \implies \exists m,n \in \mathbb{Z}$   $d = am+bn$
4. $a = qd+r \implies r = (-qm+1)a+(-qn)b \implies r < d \land r \in \text{CL}^+(a,b) \implies r = 0 \implies d | a \land d | b$
5. $c | a \land c | b \implies c | am+bn \implies c | d \implies c \leq d$

DIMOSTRAZIONE: Induzione sul numero di passi dell'algoritmo di Euclide.

Dati $a,b \in \mathbb{Z}$ con $a \neq 0 \lor b \neq 0$ vale $(a,b)= \min\text{CL}^+(a,b)$.

DIMOSTRAZIONE: Bézout diviso MCD.

Siano $a,b,c \in \mathbb{Z}$. Se $a | bc$ e $(a,b)=1$ allora $a|c$.

DIMOSTRAZIONE: Bézout diviso MCD moltiplicato $c$.

Si può ottenere Bézout applicando l'algoritmo di Euclide a ritroso.

# Equazione diofantea
Siano $a,b,c\in \mathbb{Z}$ coefficienti e $x,y\in \mathbb{Z}$ variabili. L'equazione $ax+by=c$ è detta diofantea.

L'equazione diofantea $ax+by=c$ è risolubile $\iff (a,b) | c$.

DIMOSTRAZIONE: Bézout.

Siano $(\bar{x},\bar{y})$ una soluzione dell'equazione diofantea e $(\gamma,\delta)$ una soluzione dell'equazione omogenea associata. Allora $(\bar{x}+\gamma,\bar{y}+\delta)$ è un'altra soluzione dell'equazione non omogenea.

Se un'equazione diofantea ammette soluzioni, ne ammette infinite. Inoltre tutte e sole le soluzioni sono nella forma descritta prima.

DIMOSTRAZIONE: Se $(\alpha,\beta)$ risolve l'equazione, $(\alpha-\bar{x},\beta-\bar{y})$ risolve l'omogenea associata.

Per risolvere una diofantea si può ottenere Bézout.